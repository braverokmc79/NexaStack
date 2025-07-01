# 🌐 Django Ninja vs Django 개발 가이드

---

## ✨ Django 이란?

Django는 Python으로 개발된 고수준 웹 프레임워크로, “빠른 개발”과 “간단한 구조”를 강조한다.

### ▶️ 주요 특징:

- MTV (Model - Template - View) 그룹
- 간편한 ORM 지원
- 관리자 인터페이스 자당 생성
- 보안: CSRF, XSS, SQL Injection 등 예보
- 통합적 관리, 회사 구조에 적합

---

## 🚀 Django Ninja 라는?

**Django Ninja**는 Django 개발 경험을 기반으로 하며, **FastAPI 형식의 고객을 지원하는 API 프레임워크**다.

### ▶️ 특징:

- Python 3.6+의 **타입 힌트 기반**
- 구조 간단 & 사용 쉽는 API 만들기
- **Swagger, ReDoc 문서**를 자당적으로 생성
- **Pydantic**을 이용한 입·출력 데이터 검증
- Django ORM, 인자 권한, 추가프로세스 등과 그리고 각종 Django 구조와 가변이 유용

---

## 📊 Django vs Django Ninja 비교

| 아위     | **Django**              | **Django Ninja**        |
| ------ | ----------------------- | ----------------------- |
| 사용 방식  | MTV 그룹 구조               | FastAPI식 Router         |
| 관심사    | 웹 전체 구조                 | API 중심 RESTful 구조       |
| 프리로세스  | View / Template / Form  | @api.get(), @api.post() |
| 데이터 검증 | Form, Serializer (DRF)  | Pydantic Model          |
| API 문서 | 계가적으로 건설                | Swagger / ReDoc 자당 생성   |
| 비디오    | DRF + Swagger 그리고 복수 구조 | FastAPI와 같은 간단한 구조      |

---

## 🔧 Django Ninja 연결 예시

```python
# apis/api.py
from ninja import NinjaAPI
from django.http import HttpRequest

api = NinjaAPI()

@api.get("/hello")
def hello(request: HttpRequest, name: str):
    return {"message": f"Hello {name}"}
```

- `@api.get("/hello")` : 데이터 검증 + 리원지 API URL
- Swagger UI 또는 ReDoc에서 자동 문서화

---

## ⚖️ Django REST Framework vs Django Ninja

| 아위     | Django REST Framework | Django Ninja       |
| ------ | --------------------- | ------------------ |
| 건설 복지  | 관련 필요 설정 많음           | 간단, 쉽게 설정          |
| 타입 힌트  | 부담적 (일반 설치)           | 전멸 지원              |
| API 문서 | drf-yasg 등 구설 필요      | Swagger / ReDoc 자당 |
| 비디오    | 그리 건설 필요              | 설치 필요 X            |
| 도입/리스트 | Serializer 기반         | Pydantic 기반        |

---

## 📅 경험자 간단 치환:

- Django을 이미 알고 있다면, **Django Ninja는 더 방울리스러워진 DRF** 보다 쉽게 REST API를 구축 가능
- Swagger UI로 API 문서 보게 되고, 다양한 개발 규모에 적적
- 테스트가 느림없고, MVP 조금씩 만들더라도 편리

---

## ✅ 경험자 목적 정보:

- “DRF 여행 버공을 했는데, 더 쉽고 감각적인 것은 없을까?” 같은 것을 고민하는 경험자에게 개찰
- Django에 기반하고 있고, 타입 힌트 구조에 관심이 많고, API 지원 간겳다면 무엇보다 가장 괜찮은 해결책

