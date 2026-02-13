# openclaw_docs
## 미리 세팅해놔야 하는 것
### LLM model, chat app 등에 따라 다르다. 크게 이렇게 미리 세팅이 필요하다. 링크는 내가 진행한 것만 소개함.
- LLM api key (openai API, anthopic API 등)
  - openai API : https://platform.openai.com/login
- Chat app bot API (Telegram, whatsapp)
  - Telegram : botfather 를 검색해서 여기서 `/newbot` 입력
    - -> bot 이름 입력(ex) my_bot)
    - -> 입력하면 해당 bot token이 나오는데 그 토큰을 별도 저장해두고 openclaw에 입력해줘야 함
    - -> botfather 에서 나와서 검색에 my_bot 입력해서 들어가기
    - -> 여기서 openclaw 게이트웨이가 켜진 상태에서 /start 입력하면 pairing token이 나옴
    - -> 이걸 openclaw에 `openclaw pairing approve telegram [your_token]` 으로 입력해주면 됨.
    - 참고 자료 : https://midoriiroplace.tistory.com/62
- brave search api (웹 검색 API)
  - https://brave.com/search/api/
  - 이게 필요한 이유는 robots.txt 등의 문제로 검색이 안 되는 문제를 이 api를 통해 해결해주기 때문이다.
  - 이 api key를 등록하려면 openclaw에서 명령어에 따로 입력해줘야 하는데 아래 docker container를 이용하면 자동으로 세팅해줌.
### <br/><br/><br/>


## 세팅 방법
### Docker hub에 자세히 써놓았다. 
- https://hub.docker.com/r/shinejh0528/openclaw
