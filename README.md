# 🚀 Spring Cloud Gateway 핵심 개념 정리

## 📚 공식 문서
🔗 [Spring Cloud Gateway 공식 Reference Guide](https://docs.spring.io/spring-cloud-gateway/docs/current/reference/html/#gateway-request-predicates-factories)

---

## 🧩 핵심 개념

### 🌐 Route (라우트)
> 클라이언트의 요청을 **“어디로 보낼지”** 결정하는 규칙

- 예: `/api/user/**` 요청을 `user-service` 로 전달
- 하나의 Gateway에는 여러 개의 Route를 설정 가능

---

### ⚙️ Predicate (조건)
> 특정 조건에 따라 **Routing 수행 여부를 결정**

- 요청의 속성을 기반으로 판단 (Path, Header, Method, IP 등)
- 예:
  ```yaml
  predicates:
    - Path=/api/**