# # 웹 채팅을 위한 API 기능들

### 디렉토리 구조 및 설명
```bash
├── common  # 공통으로 쓰이는 함수 모음
│   ├── __init__.py
│   └── lib.py  # 자주 쓰이는 함수들
├── core  # API 기능을 위한 공통 환경 변수들
│   ├── __init__.py
│   └── config.py  # 환경변수
├── db
│   ├── models
│   │   ├── __init__.py
│   │   └── table_model.py  # 실제 데이터베이스에 존재하는 테이블 스키마
│   ├── __init__.py
│   ├── connection.py  # 데이터베이스 세션 호출 시작 및 닫는 역할
│   └── session.py  # 데이터베이스 세션 생성
├── modules  # 연동된 데이터베이스에서 create, read, update, delete가 들어간 api 기능 관련 요소들을 모듈별로 분류
│   ├── __init__.py
│   ├── chat.py  # 채팅 API기능 관련 DB 쿼리
│   ├── token.py  # 토큰 API기능 관련 DB 쿼리
│   └── user.py  # 사용자 API기능 관련 DB 쿼리
├── routes  # 각 모듈별로 URL을 분류해주는 라우터
│   ├── __init__.py
│   ├── chat.py  # 채팅 관련 API
│   ├── token.py # 토큰 관련 API
│   └── user.py  # 사용자 관련 API
├── schemas  # pydantic 모델 스키마 설정 --> FastAPI의 POST방식 API의 BODY에 들어갈 데이터 형식 설정  
│   ├── __init__.py
│   ├── chat.py  # 채팅 관련 pydantic 스키마들
│   ├── token.py # 토큰 관련 pydantic 스키마들
│   └── user.py  # 사용자 관련 pydantic 스키마들
├── __init__.pt
└── main.py  # API 실행 시작 부분
``` 
