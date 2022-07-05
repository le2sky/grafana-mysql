## Step01.Grafana 구성

요구사항

- Grafana의 3000번 포트는 호스트의 3000번 포트와 바인딩
- Grafana의 설정파일인 grafana.ini는 호스트에서 주입 가능하도록 구성하고 읽기 전용 설정
- Grafana의 로컬 데이터 저장 경롤를 확인하여 도커 볼륨 마운트
- Grafana의 플러그인 추가 설치를 위한 환경변수 설정
- 로그 드라이버 옵션을 통해 로그 로테이팅

## Step02. Grafana + MySQL 구성

요구사항

- 1단계 요구사항을 포함
- grafana.ini를 통해 database 설정을 sqlite에서 MySQL로 변경
- MySQL 컨테이너를 docker-compose에 db 서비스로 추가
- grafana 서비스가 db 서비스를 database로 연결하도록 구성
- MySQL의 로컬 데이터 저장 경로 확인하여 도커 볼륨 마운트
