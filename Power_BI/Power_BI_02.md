# Power BI_Basic



### 열 제거

- [총합계] 열에서 [제거] 선택

- 열 오른쪽 마우스 클릭 – [제거]



---



### 행 제거

- 1행의 Null 제거

- [홈] – [행 제거] – [상위 행 제거] 선택, 삭제할 행 수 입력
- [첫 행을 머리글로 사용] 클릭



---



### 채우기

- 빈 공간이 있을 때 사용한다.
- 연도 필드의 Null 값 채우기
- [연도] 필드에서 마우스 오른쪽 단추
- [채우기] – [아래로] 선택
- 2019년이 다음 입력값이 있을 때까지 빈 공간을 채워준다.



---



### 값 바꾸기

- 년도의 문자 제거

- [값 바꾸기] 선택하여 찾을 값, 바꿀 항목 입력 후 [확인] 클릭



---



### 날짜 변환

- 주문월의 형식을 ‘월’로 변경

- [변환] – [월] – [월] 선택



---



### 열 피벗 해제

- 열로 구성된 데이터를 행으로 데이터 변환

- [서울~대구]까지 필드 선택 후(Shift 이용) → [열 피벗 해제] 선택

- 데이터가 Null인 경우 행으로 표시되지 않음

- 열을 행으로 바꿀 때 사용한다.



---



### DAX 언어

- 총수량 = SUM('판매'[수량])
- 매출금액 = '판매'[단가] * '판매'[수량] * (1-'판매'[할인율])
  - 할인율까지 계산하기 위해 1-할인율을 해줌
- 매출원가 = '판매'[원가] * '판매'[수량]
- 매출이익 = '판매'[매출금액] - '판매'[매출원가]
- 매출원가 = RELATED('제품'[원가]) * [수량]
  - 해당 테이블에 원가가 없을 경우
  - 다른 테이블의 필드를 가져올 수 있음
- 총매출금액 = SUM('판매'[매출금액])
- 총매출이익 = SUM('판매'[매출이익])
- 매출이익률 = DIVIDE([총매출이익], [총매출금액], 0)
  - 총매출 이익을 총매출금액으로 나눔
  - 마지막 0은 값이 없을 때 0 값을 넣어줌
- 시도(map) = IF([시/도] = "강원도", "강원도(Gangwon)", [시/도])
  - [시/도] 필드에서 값이 만약 '강원도'라면 '강원도(Gangwon)'로 나타내라. 아니면 그냥 [시/도] 값을 써라.
- 주소 = [시/도]&" "&[구/군/시]
  - 새열 추가
  - 값은 [시/도] 필드와 [구/군/시] 필드를 합친 것
  - 둘 사이의 공백표시 " "
  - &&으로 연결
- 총이용자수 = COUNTROWS('대여이력')
  - 테이블의 전체 행의 수
  - 대여 이력의 총 수가 곧 총 이용자 수를 나타낸다.
  - 이러한 접근 생각을 할 필요가 있음
- 총대여소수 = COUNTROWS('대여소현황')
- 총거치대수(QR) = SUM([거치대수(QR)])



---



### 도형맵

- [도형맵] 생성
- [위치]에 [시/도] 넣기
- [색 채도]에 [매출금액] 넣기
- 서식 툴에서 지도 설정. 하지만 지도에 한국이 없음 >> 따로 설정을 해줘야 함
- 사용자 설정으로 지정
- korea.Simple json 파일 사용
- 이렇게 한국 지도를 사용하려면 그에 맞는 json 파일을 구할 줄 알아야 함



---



### 필터

- 툴 가장 왼쪽에 필터가 자동으로 보여짐
- 여기서 조건부 서식을 지정할 수 있음
- 모든 페이지에 필터
- 시도 삽입
- 시도별로 필터링할 수 있음



---



### 열 분할

- [Contry] 필드에서 [b], (US) 등 제거
- [열 분할] – [구분 기호 기준]

- 사용자 지정 설정 후 '[’, ‘(’ 기준으로 나누기
- 불필요한 열 제거
- 데이터 변환 작업 완료 후 [홈] – [닫기 및 적용] 클릭



---



### Power BI 수업을 듣고 느낀점

​	Power BI는 PPT와 같다. 누구나 PPT를 만들 수 있는 것처럼 Power BI도 누구나 만들 수 있다. 하지만 얼마나 많이 경험하냐에 따라 질이 달라진다. 더 다양한 기능을 사용할 수 있고, 시각화를 더 이쁘게 할 수 있다. 현재 나에게 PPT 작업이 익숙한 것처럼 Power BI도 꾸준히 연습해 놓자.
