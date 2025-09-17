#도커 이미지 생성 연습 입니다. 
/# 1. 작업 폴더 생성<br>
mkdir  ~/dockerimage && cd ~/dockerimage<br>

/# 2. nginx:alpine 받기<br>
docker pull nginx:alpine<br>

/# 3. Dockerfile 생성<br>
vi Dockerfile # 상세 내용은 첨부 파일 참고<br>

/# 4. 도커 네트워크 생성<br>
docker network create {네트워크 이름}<br>

/# 5. 이미지 빌드<br>
docker build --no-cache -t {사용자명/이미지이름[:태그]} . <br>

/# 6. 컨테이너 생성 & 실행<br>
docker run -d --name mygame -p 8080:8080 \\<br>
    --network ongamenet \\<br>
    mygameimage<br>

/# 7. 웹으로 확인<br>
firefox http://192.168.10.10:8080/{실행파일명.html} <br>

 도커 이미지 실습 주소입니다 :)<br>
[Snake Game]<br>
https://hub.docker.com/r/haeyoun/gameimage1<br>
<br>
[Block-It Game]<br>
https://hub.docker.com/r/haeyoun/gameimage2<br>
<br>
[Bubble-Shooter]<br>
https://hub.docker.com/r/haeyoun/gameimage3<br>
