# 데이터의 이해



### 데이터 정의

​	데이터란 개별 데이터 자체로는 의미가 중요하지 않은 객관적 사실(fact)이다. 추론, 예측, 전망, 추정을 위한 근거(basis)이며 다른 객체와의 상호 관계 속에서 가치를 갖는다.



---



### 데이터 유형

**1. 정성적 데이터**
   - 언어, 문자로 기술
   - 비정형 데이터 형태로 저장, 분석에 시간과 비용이 필요
   - ex) 설문조사의 주관식 응답, SNS 글, 기상특보

**2. 정량적 데이터**

   - 수치, 기호, 도형으로 표시
   - 데이터 양이 증가하더라도 저장, 분석이 용이
   - ex) 지역별 온도, 풍속, 강우량



---



### 암묵지 & 형식지

**1. 암묵지**
   - 학습과 체험을 통해 개인에게 습득
   - 시행착오와 오랜 경험을 통해 습득된 무형 지식
   - 공유되기 어려움
   - ex) 자전거 타기

**2. 형식지**

   - 교과서, 매뉴얼, DB 등 형상화 된 지식
   - 외부로 표출되어 여러 사람이 공유할 수 있는 지식
   - 회계, 재무 관련 대차대조표에 요구되는 지식 매뉴얼



---



### 지식경영

**1단계 공통화(암-암)**: 암묵적 지식 노하우를 다른 사람에게 알려주는 것

**2단계 표출화(암-형)**: 암묵적 지식 노하우를 책이나 교본 등 형식지로 만드는 것

**3단계 연결화(형-형)**: 내가 알고 있는 지식을 책이나 교본 등에 추가하는 것

**4단계 내면화(형-내)**: 만들어진 책이나 교본 등을 보고 다른 직원들이 암묵적 지식을 습득하는 것



---



### DIKW

**D**ata: 다른 데이터와 상관관계가 없는, 가공하기 전 순수한 수치나 기호

**I**nformation: 데이터 가공 및 상관/연관 관계 속에서 의미를 도출하는 것

**K**nowledge: 상호 연결된 정보 패턴을 이해하여 이를 토대로 예측한 결과물

**W**isdom: 근본 원리에 대한 깊은 이해를 바탕으로 도출된 아이디어

​	ex) 

​		A마트 = 200원, B마트 = 300원

​		A마트가 B마트보다 싸다.

​		A마트가 상대적으로 더 저렴하니 A마트에서 사야겠다.

​		A마트의 다른 상품들도 더 쌀 것이라 판단.



---



### DataBase 특징

1. **통합 데이터**: 데이터베이스 내 같은 내용의 데이터가 중복되어 있지 않는다.
2. **저장 데이터**: 컴퓨터가 접근할 수 있는 저장매체에 저장되어 있다.
3. **공용 데이터**: 여러 사용자에게 서로 다른 목적으로 데이터베이스의 데이터를 공동으로 이용할 수 있다.
4. **변화되는 데이터**: 추가, 삭제, 갱신으로 변화하면서도 항상 현재의 정확한 데이터를 유지해햐 한다.



---



### DBMS

​	DataBase Management System으로 사용자와 데이터베이스 사이에서 사용자의 요구에 따라 정보를 처리해주고 데이터베이스를 관리해주는 소프트웨어.

**1. RDBMS**
   - 관계형 데이터베이스 관리 시스템
   - 정형화된 테이블로 구성된 데이터 항목들의 집합체
   - MySQL, Oracle Database
   - SQL - RDBMS의 데이터를 관리하기 위해 설계된 특수 목적의 프로그래밍 언어

**2. ODBMS**

   - 객체 지향 데이터베이스 관리 시스템
   - 객체들을 생성하여 계층에서 체계적으로 정리
   - 상위 계층으로부터 속성과 방법들을 상속받을 수 있음
   - 복잡한 데이터 구조를 표현 및 관리



---



### 데이터베이스 설계 절차

1. 요구조건 분석: 데이터베이스 사용자, 사용목적, 사용범위 등을 정리, 명세서 작성
2. 개념적 설계: E-R 모델, 정보를 추상적 개념으로 표현하는 과정. 
3. 논리적 설계: 자료를 컴퓨터가 이해할 수 있도록 특정 DBMS를 논리적 자료 구조로 변환
4. 물리적 설계: 논리적 구조 데이터를 물리적 구조의 데이터로 변환하는 과정



---



### NoSQL

​	관계형 데이터베이스보다 덜 제한적인 일관성 모델을 이용하는 메커니즘을 제공한다. 디자인 단순화, 수평적 확장성, 세세한 통제 등을 포함한다. 그리고 기존 RDBMS가 갖고 있는 특성 뿐만 아니라 다른 특성들을 부가적으로 지원한다.



- MongoDB: 데이터 교환시 BSON(Binary JSON)문서 형태로 저장하여 여러 서버에 분산 저장 및 확장이 용이. 방대한 데이터 처리가 빠르다는 장점이 있다. C++로 작성.
- Apache HBase: 하둡 플랫폼을 위한 공개 비관계형 분산 데이터베이스. 자바로 작성.
- Redis: Remote Dictionary Server의 약자. "키-값" 구조의 비정형 데이터를 저장하고 관리하기 위한 오픈 소스 기반.