# FastAPI/WebSockets

[WebSockets client](https://fastapi.tiangolo.com/ko/advanced/websockets/?h=websoc)  

통상적인 HTTP 통신은 정보가 변할 때, 클라이언트에서 요청을 보내는 경우에만 응답하는 구조이다.  
(한번의 요청, 한번의 응답으로 끝나는 구조)

반면에, WebSockets 는 한번의 요청으로 계속해서 데이터를 받을 수 있는 채널이 열리게되어 데이터를 끝없이 받을 수 있다.  
실시간으로, 주기적으로 업데이트 되어야 하는 페이지에 적합하다.  
(한번의 요청, 지속적인 응답, 채널을 닫을때까지 지속)  

### Install
```bash
python3 -m pip install uvicorn[standard] websockets
```

### examples
```python
from fastapi import FastAPI, WebSocket
from fastapi.responses import HTMLResponse

app = FastAPI()

html = """
<!DOCTYPE html>
<html>
    <head>
        <title>Chat</title>
    </head>
    <body>
        <h1>WebSocket Chat</h1>
        <form action="" onsubmit="sendMessage(event)">
            <input type="text" id="messageText" autocomplete="off"/>
            <button>Send</button>
        </form>
        <ul id='messages'>
        </ul>
        <script>
            var ws = new WebSocket("ws://localhost:8000/ws");
            ws.onmessage = function(event) {
                var messages = document.getElementById('messages')
                var message = document.createElement('li')
                var content = document.createTextNode(event.data)
                message.appendChild(content)
                messages.appendChild(message)
            };
            function sendMessage(event) {
                var input = document.getElementById("messageText")
                ws.send(input.value)
                input.value = ''
                event.preventDefault()
            }
        </script>
    </body>
</html>
"""


@app.get("/")
async def get():
    return HTMLResponse(html)


@app.websocket("/ws")
async def websocket_endpoint(websocket: WebSocket):
    await websocket.accept()
    while True:
        data = await websocket.receive_text()
        await websocket.send_text(f"Message text was: {data}")

```
