# 몽고디비 User 구현 예제 코드

---

```jsx
UserSchema

name
roles (default : "일반")
email
password
role (0 일반 유저, 1은 관리자, 임시로 넣어둠 사용 x)
token
```

## 회원가입 api

---

```jsx
POST: localhost: 5000 / api / user / signup;
```

```jsx
post값

{
"name" : "testName",
"email" : "test3@naver.net",
"password" : "test1234"
}
```

이메일 중복 방지 걸어둠

## 로그인 api

---

```jsx
POST: localhost: 5000 / api / user / login;
```

```jsx
post 값

{
"email" : "test3@naver.net",
"password" : "test1234"
}
```

토큰생성 확인



## 로그아웃 api

---

```jsx
GET: localhost: 5000 / api / user / logout;
```



clearCookie 확인

res.redirect("/");으로 처리중
