### 👷 CICD?
: 애플리케이션 개발 단계를 자동화하여 보다 짧은 주기로 유저에게 제공하는 방법
- CI : Continuous Integration, 지속적인 통합, 릴리즈를 준비하는 단계, 빌드~테스트까지의 단계(자동화 된)
- CD
  - Continuous Delivery (배포 자동화 X)
  - Continuous Deployment (배포 자동화 O)
#
### :test_tube: 과정
`CODE` ⇒ `BUILD` ⇒ `TEST` ⇒ `RELEASE` ⇒ `DEPLOY`
#
### :monocle_face: CICD 가 필요한 경우!
- 빈번한 머지
- 빌드, 테스트, 머지의 자동화의 수요
#
### :goal_net: 기대할 수 있는 효과
- 개발 생산성/효율성 향상
- 빠른 이슈 트래킹
- 버그 수정 용이
- 고립된 유닛 테스트 가능
- 코드 퀄리티 향상
#
### :bookmark: CICD 플랫폼 비교
#### Jenkins
- 무료
- 레퍼런스와 커뮤니티가 크다
- 플러그인 생태계
- Windows, MacOS 와 다양한 Linux OS 지원

#
#### Bamboo
- 유료
- Atlassian에서 개발
- `Jira`, `confluence` 와의 유기적인 연동
- Windows, MacOS 와 다양한 Linux OS 지원

#
#### ✔️  Travis CI
- 무료(public repo) / 유료(기업버전, private repo, $69)
- 간결하고 직관적인 웹 인터페이스
- `Github` 과 연동하여 Commit/Push 를 기반으로 CI를 자동화할 수 있고, PR에도 반응하도록 설계 가능

#
#### Circle CI
- 한도 내에서 무료(한주에 2500 크레딧=한달에 1000분, 한번에 하나의 job수행) / 유료 한달에 $15
- Windows, MacOS 와 다양한 Linux OS 지원

#
#### TeamCity
- DevOps 파이프라인을 세부적으로 시각화
- `Jetbrains IDE` 와 연동하면 IDE 내에서 빌드, 확인, 자동화 테스트까지 수행 가능
- 테스트 기록을 유지해주고 불안정한 테스트의 경우 신뢰도 낮음으로 표시
- Windows, MacOS 와 다양한 Linux OS 지원

#
#### Conclusion
- [ ] Jenkins : 완전 무료, 많은 레퍼런스, 하지만 젠킨스 서버가 죽거나 문제가 생기면 대처가 어려움, UI가 안이쁨  
- [ ] Bamboo : 회사 내부적으로 Jira를 쓸때 효과적임, 유료  
- [x] **Travis CI : Github와 연동할 수 있고 무료로 사용가능, 하지만 회사에서 사용시 Private repo 이므로 비용발생**  
- [ ] Circle CI : Github와 연동할 수 있고 일정수준까지 무료로 사용가능, 실제로 사용시 비용발생은 피할 수 없음  
- [ ] TeamCity : UI가 사용하기 편한데, VScode 와 연동이 어렵다.  
