## Run Spring Boot application
```
mvn spring-boot:run
```

## Run following SQL insert statements
```
CREATE TABLE `roles` (
`id` int NOT NULL,
`name` varchar(45) DEFAULT NULL,
PRIMARY KEY (`id`)
);
```

```
INSERT INTO roles(name) VALUES('ROLE_USER');
INSERT INTO roles(name) VALUES('ROLE_MODERATOR');
INSERT INTO roles(name) VALUES('ROLE_ADMIN');
```
### Sign Up:
```

URL: http://localhost:8080/api/auth/signup 
Method: POST
Request: {
"username": "Aarti",
"email": "aarti.jangid@gmail.com",
"role": ["mod"],
"password":"AartiJangid"
}
Response: {
"message": "User registered successfully!"
}
```

### Sign In:
```
URL: http://localhost:8080/api/auth/signin
Method: POST
Request: {
"username": "Aarti",
"password":"AartiJangid"
}
Response: {
"id": 1,
"username": "Aarti",
"email": "aarti.jangid@gmail.com",
"roles": [
"ROLE_MODERATOR"
],
"accessToken": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJBYXJ0aSIsImlhdCI6MTYyNDczMDQzNSwiZXhwIjoxNjI0ODE2ODM1fQ.1YBt-0fPtIz_Gzf_boZMUKvqj2iD5e45UKT3oBBZwWod27BHQsas9QyXzH8a2NgB0Fi80QLvSXVMR9jDUgkoKQ",
"tokenType": "Bearer"
}
```