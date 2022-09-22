# SSH Tricks

### SSH login header
```bash
vi /etc/update-motd.d/00-header
```

```bash
#!/bin/bash
echo -e "
띄우고 싶은 문구 ...
...
...
...

"
```
