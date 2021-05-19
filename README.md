# Postgres, Django, Nginx Dockerizing

## 개발환경

- 기본 Django 개발 서버를 사용합니다.

- docker-compose.yml 및 .env.dev 파일 에서 환경 변수를 업데이트 합니다.

- 이미지를 빌드하고 컨테이너를 실행하십시오.

```
$ docker-compose up -d --build
```

http://localhost:8000 에서 테스트 해보십시오 . "app"폴더가 컨테이너에 마운트되고 코드 변경 사항이 자동으로 적용됩니다.

## 운영환경

- gunicorn + nginx를 사용합니다.

- .env.prod 및 .env.prod.db  환경 변수를 업데이트하십시오.

- 이미지를 빌드하고 컨테이너를 실행하십시오.

```
$ docker-compose -f docker-compose.prod.yml up -d --build
```

http://localhost:1337 에서 테스트하십시오 . 마운트 된 폴더가 없습니다. 변경 사항을 적용하려면 이미지를 다시 작성해야합니다.