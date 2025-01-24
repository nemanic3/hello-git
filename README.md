# 다독다독 API 명세서

## 1. 사용자 관리

### 1.1 회원가입
- **Method:** POST
- **Endpoint:** `/users/signup/`
- **Description:** 회원가입 처리
- **요청 데이터:**
  - `username`: 사용자 이름 (string, 필수)
  - `password`: 비밀번호 (string, 필수)
  - `nickname`: 사용자 닉네임 (string, 필수)
  - `email`: 사용자 이메일 (string, 필수)
- **응답 예시:**
  ```json
  {
      "id": 1,
      "username": "example_user",
      "nickname": "example_nickname",
      "email": "example@example.com"
  }
에러 메시지:
400 Bad Request: 잘못된 데이터 제공
json
복사
편집
{"error": "Invalid data. Please check the provided information."}
409 Conflict: 중복된 username 또는 email
json
복사
편집
{"error": "Username or email already exists."}
