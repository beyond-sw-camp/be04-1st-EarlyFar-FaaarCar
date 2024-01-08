# 멀리카아

![img_reference_09](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/blob/e7fe4e7cb4a1f53f0d6050c2820bd6c73bfb1758/image/%EB%A9%80%EB%A6%AC%EC%B9%B4%EC%95%84.png)

### 팀명: 얼리멀리(Early&amp;Far) 3조
### 팀원
- 팀원 : [이준형](https://github.com/jhlee6515)
- 팀원 : [이재원](https://github.com/jlee38266)
- 팀원 : [송동준](https://github.com/dongjunsong)
- 팀원 : [정태원](https://github.com/t4e1)
- 팀원 : [신동호](https://github.com/letsplaycoding)
- 팀원 : [최종찬](https://github.com/CJC0512)

---

# 제안요청서

# 1. 프로젝트 개요

멀리카아 프로젝트는 급격하게 성장 하는 중고차 시장에서 발생하는 수많은 거래와 정보를 데이터베이스로 구축하여 다양한 정보를 체계적으로 관리하고 활용하는데 그 목적이 있습니다. 프로젝트의 추진배경은 다음과 같습니다.

## 1-1 필요성

한국 국토교통부 데이터 통합 채널에서 제공한 ‘자동차등록현황보고’ 통계에 따르면 전국적으로 자동차등록현황은 2010년을 기준으로 10년 동안 자동차에 대한 수요는 계속해서 증가하고 있다. 또한 국내 거대 규모 중고차 거래 플랫폼 중 하나인 KB차차차의 중고차 매물건수는 론칭했던 2016년 기준 15,247대에서 2018년에는 100,000대가 돌파되면서 2년 만에 8배 이상의 중고차 매물이 늘어 나는 것이 확인되었다. 결과적으로 중고차 시장의 급격한 성장으로 인해서, 수많은은 거래 및 정보가 생성되고 있고 이에 따라 중고차 관련 정보를 체계적으로 관리하여 금융 프로세스를 향상시킬 필요성이 생겼습니다.

![img_reference_01](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/45275759/008288ed-4294-488f-9010-7a8689ad5ad9)
                                  *사진 1:자동차등록현황 및 이륜차신고현황*

![img_reference_02](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/45275759/82be86db-5b9f-491a-a15b-83dd63bf48fd)
                                     *사진 2: KB차차차 중고차 등록매물 건수*

# 2. 프로젝트 작업 범위

멀리카아 프로젝트의 예상 결과물은 다양한 측면에서 중고차 데이터베이스의 구축 하기 위해 활용되는 항목들이 있으며 아래와 같습니다.

- 중고차 데이터베이스: 중고차 관련 정보를 체계적으로 수집, 저장, 관리하는 데이터베이스의 구축 및 운영
- 개체-관계 다이어그램(ERD) 및 테이블 정의: 중고차 데이터베이스의 구조를 명확히 나타내는 ERD와 각 테이블에 대한 정의서
- SQL 쿼리 및 검색 기능: 데이터베이스에서 중고차 정보를 검색하고 분석하기 위한 기본 및 복잡한 SQL 쿼리 및 검색 기능
- 프로젝트 문서 및 메뉴얼: 프로젝트 진행 과정, 진행 장소 및 프로젝트 구현 도구
- 테스트 결과 보고서: SQL 쿼리 및 시스템 기능에 대한 테스트 결과를 기록한 테스트 결과 보고서

## 2-1 추진 계획

                                             *테이블 1: 추진체계*

| 구분 | 조직 | 주요 역할 |
| --- | --- | --- |
| 주관 | 팀 얼리멀리 (Early & Far) | 데이터 베이스 구축 |
| 지원기관 | 한화시스템x엔코아 | 장비 지원 및 퀄리티 점검 |

추진 일정: 2023-12-30 ~ 2024-01-08

작업 수행공간: 서울 동작구 보라매로 SFC빌딩, 원격 소통

프로젝트 구현 도구: MariaDB 10.11.6-GA, Linux Ubuntu 20.04.6 LTS

## 2-2  일정관리 (WBS)

![img_wbs](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/45275759/1bac9e91-1146-4d6e-84f4-4aea6f54e562)

# 3. 요구사항

요구사항 항목에서는 프로젝트 데이터베이스 구현에 필요한 기능적, 비기능적 요구사항 파악과 구현을 위한 구체적인 명세서 그리고 모델링과 모델 테스트 결과를 확인할 수 있습니다.

## 3-1 작업 명세서
<details>
<summary>요구사항 명세서</summary>
<div markdown="1">

| 요구사항 ID | 기능유형(기능/비기능) | 요구사항명 | 요구사항 내용 | 중요도(상/중/하) | 수용여부(O/X) |
| --- | --- | --- | --- | --- | --- |
| REQ001 | 기능 | 회원 가입 | 사용자는 중고차 거래 사이트에 회원으로 가입할 수 있어야 함 | 상 | O |
| REQ002 | 기능 | 회원 탈퇴 | 회원은 원한다면 언제든지 회원 탈퇴 할 수 있어야 함 | 상 | O |
| REQ003 | 기능 | 로그인 | 등록된 회원은 아이디와 비밀번호를 사용하여 로그인할 수 있어야 함 | 상 | O |
| REQ004 | 기능 | 로그아웃 | 회원은 언제든지 로그아웃 할 수 있어야 함 | 중 | O |
| REQ005 | 기능 | 비밀번호 재설정 | 회원은 비밀번호를 분실한 경우, 이를 재설정할 수 있는 링크를 받을 수 있어야 함 | 중 | O |
| REQ006 | 기능 | 프로필 수정 | 회원은 개인 정보 및 닉네임 등을 언제든지 수정할 수 있어야 함 | 중 | O |
| REQ007 | 기능  | 회원 권한 | 회원은 등급별로 권한을 부여받아야 함 | 상 | O |
| REQ008 | 기능 | 게시물 검색 | 사용자는 다양한 조건으로 게시물을 검색할 수 있어야 함 | 상 | O |
| REQ009 | 기능 | 거래 예약 등록 | 회원은 시승, 거래 상담 등의 사유로 중고차 거래를 예약할 수 있어야 함 | 중 | O |
| REQ010 | 기능 | 거래 등록 | 회원은 중고차를 판매하거나 구매하기 위해 게시물을 등록할 수 있어야 함 | 상 | O |
| REQ011 | 기능 | 알림 수신 설정 | 회원은 중요한 거래 알림을 설정하고 수신할 수 있어야 함 | 중 | O |
| REQ012 | 기능 | 판매자 평가 | 거래 완료 후 구매자는 판매자를 평가하고 리뷰를 남길 수 있어야 함 | 중 | O |
| REQ013 | 기능 | 리뷰 확인 및 관리 | 회원은 자신에게 작성된 리뷰를 확인하고 부적절한 리뷰를 신고할 수 있어야 함 | 중 | O |
| REQ014 | 기능 | 쿠폰 발급 및 관리 | 사이트에서 회원에게 쿠폰을 발급하고, 회원은 쿠폰을 관리(사용)할 수 있어야 함 | 중 | O |
| REQ015 | 기능 | 할인 적용 | 회원은 거래 시 발급 받은 쿠폰을 사용하여 할인 혜택을 받을 수 있어야 함 | 중 | O |
| REQ016 | 기능 | 사용자 신고 | 회원은 사이트 규율을 위반한 다른 회원을 신고할 수 있어야 함 | 중 | O |
| REQ017 | 기능 | 차량 정보 등록 | 판매자는 중고차의 기본 정보를 등록할 수 있어야 함 | 상 | O |
| REQ018 | 기능 | 차량 이미지 업로드 | 판매자는 중고차에 대한 이미지를 업로드할 수 있어야 함 | 중 | O |
| REQ019 | 기능 | 가격 및 거래 조건 등록 | 판매자는 중고차의 판매 가격 및 거래 조건을 등록할 수 있어야 함 | 상 | O |
| REQ020 | 기능 | 차량 상태 및 특이사항 등록 | 판매자는 중고차의 현재 상태, 사고 이력, 정비 이력 등을 자세히 등록할 수 있어야 함 | 중 | O |
| REQ021 | 기능 | 차량 검색 및 필터링 | 회원은 중고차 목록을 다양한 기준으로 검색하고 필터링할 수 있어야 함 | 상 | O |
| REQ022 | 기능 | 차량 관심 등록 및 알림 | 회원은 특정 차량을 관심 목록에 등록하고, 해당 차량에 대한 가격 변동 등 알림을 받을 수 있어야 함 | 중 | O |
| REQ023 | 기능 | 차량 상세 정보 조회 | 회원은 각 차량에 대한 상세 정보를 확인할 수 있어야 함 | 상 | O |
| REQ024 | 기능 | 중고차 경매 기능 | 시스템은 중고차 경매 기능을 제공하여 회원 간의 경매를 통해 차량을 판매하거나 구매할 수 있어야 함 | 하 | O |
| REQ025 | 기능 | 추가 조항 및 특이사항 | 시스템을 통해 중고차 결제 시, 환불/교환 정책, 특정 조건에 대한 합의 사항 등이 화면을 통해 제시되어야 함 | 상 | O |
| REQ026 | 기능 | 서명 | 시스템을 통해 중고차 결제 시, 구매자 및 판매자의 서명 및 날짜가 화면을 통해 제시되어야 함 | 상 | O |
| REQ027 | 기능 | 소유권 이전 및 문서  | 시스템을 통해 중고차 결제 시, 등록증, 소유권증, 소유권 이전 절차 등이 화면을 통해 제시되어야 함 | 상 | O |
| REQ028 | 비기능 | 로그인 속도 | 로그인은 1초 미만의 짧은 속도로 이뤄져야 함 | 중 | O |
| REQ029 | 비기능 | 보안 | 사용자 개인 정보는 안전하게 저장되어야 하며, 암호화된 통신을 사용해야 함 | 상 | O |
| REQ030 | 비기능 | 거래 안전성 | 거래는 안전하게 이루어져야 하며, 부정거래 방지를 위한 보안 기능이 필요함 | 상 | O |
| REQ031 | 비기능 | 실시간 통지 | 중요한 거래 관련 사항에 대한 실시간 푸시 알림이 제공되어야 함 | 중 | O |
| REQ032 | 기능 | 신고 절차 및 양식 | 회원은 부적절한 행동에 대한 신고를 할 수 있는 절차와 양식이 제공되어야 함 | 상 | O |
| REQ033 | 비기능 | 익명 신고 | 회원은 자신을 식별하지 않고 익명으로 신고를 제출할 수 있어야 함 | 중 | O |
| REQ034 | 기능 | 신고 이력 조회 | 관리자는 이전에 발생한 신고 이력을 조회할 수 있어야 함 | 중 | O |
| REQ035 | 기능 | 신고 효과적인 피드백 | 회원은 신고에 대한 결과를 효과적으로 피드백 받을 수 있어야 함 | 중 | O |
| REQ036 | 기능 | 블랙리스트 관리 | 관리자는 부적절한 행동을 하는 회원을 블랙리스트에 등록하고 해제할 수 있어야 함 | 상 | O |
| REQ037 | 기능 | 블랙리스트 효과 | 블랙리스트에 등록된 회원은 특정 서비스 또는 기능에 접근할 수 없어야 함 | 상 | O |
| REQ038 | 기능 | 블랙리스트 공지 | 블랙리스트에 등록된 회원은 등록 사유와 기간에 대한 공지를 받을 수 있어야 함 | 중 | O |
| REQ039 | 기능 | 블랙리스트 조회 | 운영자 및 관리자는 블랙리스트에 등록된 회원 목록을 조회할 수 있어야 함 | 중 | O |
| REQ040 | 기능 | 블랙리스트 자동 처리 | 회원은 신고가 누적 5회 이상이 될 경우, 자동으로 블랙 리스트에 등록됨 | 중 | O |
| REQ041 | 기능 | 제재 내역 기록 | 회원의 제재 기한이 종료될 경우, 그 내역이 제재 내역에 기록되어야 한다. | 상 | O |
| REQ042 | 기능 | 로그인 제한 | 일정 시간 내, 사용자의 로그인 실패 횟수가 5회 이상인 경우, 해당 회원 아이디의 로그인이 5분 동안 제한됨. | 상 | O |
| REQ043 | 기능 | 로그인 내역 기록 | 사용자가 회원 로그인을 시도하면 그 내역이 기록되어야 함 | 상 | O |

</div>
</details>
    
  

## 3-2 개념 & 논리 모델링

![img_conceptual_model](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/45275759/045217ef-b9a9-4212-aa91-b7932ba4282d)

개념 모델링

![img_logical_model](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/45275759/b03c48f6-1596-4e5f-b285-cc946b91f521)

DA# 논리 모델

## 3-3 물리 모델링

![img_physical_model](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/45275759/b31ce7a6-d168-4507-b548-89253ca4ac6d)

DA# 물리 모델

## 3-4 DDL 구문 작성
<details>
<summary>DDL 구문</summary>
<div markdown="1">

```sql
CREATE TABLE model (
	Model_ID	VARCHAR(255)	PRIMARY KEY COMMENT '차종코드',
	Model_name	VARCHAR(255)	NOT NULL COMMENT '차종명',
	Model_description	TEXT NOT NULL COMMENT '차종 설명'
)COMMENT = '차종';

CREATE TABLE Car (
	Car_ID	INT	PRIMARY KEY AUTO_INCREMENT COMMENT '자동차 ID',
	Car_field	VARCHAR(255)	NOT NULL COMMENT '제조사',
	Car_model	VARCHAR(255)	NOT NULL COMMENT '모델',
	Car_year	INT	NOT NULL COMMENT '연식',
	Car_mileage	INT	NOT NULL COMMENT '주행거리',
	Car_condition	VARCHAR(255)	NOT NULL COMMENT '컨디션',
	Car_transmission	VARCHAR(255)	NOT NULL COMMENT '변속기',
	Car_oiltype	VARCHAR(255)	NOT NULL COMMENT '연료 종류',
	Car_engine	VARCHAR(255)	NOT NULL COMMENT '엔진 크기',
	Car_fuel_efficiency	INT	NOT NULL COMMENT '연비',
	Accident_check	TINYINT(1)	NOT NULL	DEFAULT 0 COMMENT '사고 여부',
	Inundation_check	TINYINT(1)	NOT NULL	DEFAULT 0 COMMENT '침수 여부',
	Selling_price	INT	NOT NULL COMMENT '매물가격',
	Picture_URL	VARCHAR(255)	NOT NULL DEFAULT '-' COMMENT '사진 경로',
	Picture_origin	VARCHAR(255)	NOT NULL DEFAULT '-' COMMENT '원본사진 이름',
	Picture_rename	VARCHAR(255)	NOT NULL DEFAULT '-' COMMENT '사진 이름',
	Model_ID	VARCHAR(255)	NOT NULL COMMENT '차종코드',
  Insepction_record_URL  VARCHAR(255) NOT NULL COMMENT '성능점검기록부',
  FOREIGN KEY(Model_ID) REFERENCES model (Model_ID)
)COMMENT = '자동차';


CREATE TABLE Ownership_history (
	Ownership_ID	INT	PRIMARY KEY AUTO_INCREMENT COMMENT '소유이력ID',
	Previous_Owner	VARCHAR(255)	NULL	DEFAULT '-' COMMENT '이전소유자',
	Current_Owner	VARCHAR(255)	NOT NULL COMMENT '현재소유자',
	Ownership_start	DATETIME	NOT NULL COMMENT '소유시작일',
	Ownership_end	DATETIME	NOT NULL COMMENT '소유종료일',
	Reason_transfer	TEXT	NOT NULL COMMENT '소유이전된이유',
	Descript_transfer	TEXT	NOT NULL COMMENT '소유이전된상세설명',
	Car_ID	INT	NOT NULL COMMENT '자동차 ID',
  FOREIGN KEY(Car_ID) references Car(Car_ID)
)COMMENT = '소유이력';

CREATE TABLE Accident_History (
	Accident_ID INT AUTO_INCREMENT COMMENT '차동자 사고 ID',
	Accident_damage_degree INT NOT NULL COMMENT '피해정도',
	Accident_date DATETIME NOT NULL COMMENT '발생 일자',
	Insurance_claim_check TINYINT(1) NOT NULL DEFAULT 0 COMMENT '보험청구여부',
	Car_ID INT NOT NULL COMMENT '자동차 ID',
	CONSTRAINT PK_ACCIDENT_HISTORY PRIMARY KEY (Accident_ID),
	CONSTRAINT FK_Inspection_record_TO_Accident_History_1 FOREIGN KEY (Car_ID) REFERENCES Car (Car_ID)
)COMMENT = '자동차침수이력';

CREATE TABLE Inundation (
	Inundation_ID INT	AUTO_INCREMENT COMMENT '차동자 침수 ID',
	Inundation_degree INT NOT NULL COMMENT '침수정도',
	Inundation_date DATETIME NOT NULL COMMENT '발생 일자',
	Car_ID INT NOT NULL COMMENT '자동차 ID',
	CONSTRAINT PK_INUNDATION PRIMARY KEY (Inundation_ID),
	CONSTRAINT FK_Inspection_record_TO_Inundation_1 FOREIGN KEY (Car_ID) REFERENCES Car (Car_ID)
)COMMENT = '자동차침수이력';

CREATE TABLE Member (
	Member_ID	INT	PRIMARY KEY AUTO_INCREMENT COMMENT '회원ID',
	Member_name	VARCHAR(255)	NOT NULL COMMENT '이름',
	Member_nickname	VARCHAR(255)	NOT NULL COMMENT '닉네임',
	Member_password	VARCHAR(255)	NOT NULL COMMENT '비밀번호',
	Member_email	VARCHAR(255)	NOT NULL COMMENT '이메일',
	Member_phoneNum	VARCHAR(255)	NOT NULL COMMENT '전화번호',
	Member_address	VARCHAR(255)	NOT NULL COMMENT '주소',
	Member_birth	DATETIME	NOT NULL COMMENT '생년월일',
	Member_sign_up_date	DATETIME	NOT NULL COMMENT '가입일',
	Member_coupon	INT	NULL	DEFAULT 0 COMMENT '보유 쿠폰',
	Dealer_company	VARCHAR(255)	NULL COMMENT '딜러 회사명',
	Dealer_region	VARCHAR(255)	NULL COMMENT '딜러 근무지',
	Dealer_grade	INT	NULL COMMENT '딜러 등급',
	Member_type	INT	NOT NULL COMMENT '회원 유형',
	Member_blacklist	TINYINT(1)	NULL	DEFAULT 0 COMMENT '블랙회원여부',
	Restriction_date	DATETIME	NULL COMMENT '제재 적용일',
	Restriction_end_date	DATETIME	NULL COMMENT '제재 종료일',
	Login_fail_stack	INT	NULL DEFAULT 0 COMMENT '로그인실패횟수',
	Report_issue_stack	INT	NULL DEFAULT 0 COMMENT '누적신고횟수',
	Login_restriction_check	TINYINT(1)	NULL	DEFAULT 0 COMMENT '접근제한여부',
	Member_withdraw_check	TINYINT(1)	NULL	DEFAULT 0 COMMENT '탈퇴여부',
	Member_withdraw_date DATE NULL COMMENT '탈퇴날짜'
)COMMENT = '회원';

CREATE TABLE Coupon (
	Coupon_number INT AUTO_INCREMENT COMMENT '쿠폰 번호',
	Coupon_date DATETIME NOT NULL COMMENT '발급 일자',
	Coupon_usage_status TINYINT(1) NOT NULL DEFAULT 0 COMMENT '쿠폰 사용 상태',
	Coupon_description TEXT NOT NULL COMMENT '쿠폰 설명',
	Member_ID INT NOT NULL COMMENT '회원ID',
	CONSTRAINT PK_COUPON PRIMARY KEY (Coupon_number),
	CONSTRAINT FK_Member_TO_Coupon_1 FOREIGN KEY (Member_ID) REFERENCES Member (Member_ID)
) COMMENT = '쿠폰';

CREATE TABLE Login_log (
	Login_log_ID	INT AUTO_INCREMENT COMMENT '로그인내역ID',
	Success_check	TINYINT(1)	NOT NULL	DEFAULT 0 COMMENT '성공여부',
	Attempt_date	DATE	NOT NULL COMMENT '시도날짜',
	Attempt_time	TIME	NOT NULL COMMENT '시도시간',
	Attempt_IP	VARCHAR(255)	NOT NULL COMMENT '시도경로',
	Member_ID	INT	NOT NULL COMMENT '회원ID',
	CONSTRAINT pk_Login_log_ID PRIMARY KEY (Login_log_ID),
	CONSTRAINT fk_Member_ID FOREIGN KEY (Member_ID) REFERENCES Member (Member_ID)
) COMMENT = '로그인내역';


CREATE TABLE Report (
	Report_ID	INT AUTO_INCREMENT COMMENT '신고 ID',
	Report_type	VARCHAR(255)	NOT NULL COMMENT '신고 유형',
	Report_date	DATETIME	NOT NULL COMMENT '신고 일자',
	Punish_check	TINYINT(1)	NOT NULL	DEFAULT 0 COMMENT '처벌 여부',
	Report_substance	TEXT	NOT NULL COMMENT '신고 내용',
	Reporter_ID	INT	NOT NULL COMMENT '신고자 ID',
	Reported_ID	INT	NOT NULL COMMENT '피신고자 ID',
	CONSTRAINT pk_Report_ID PRIMARY KEY (Report_ID),
  CONSTRAINT fk_Reporter_ID FOREIGN KEY (Reporter_ID) REFERENCES Member (Member_ID),
	CONSTRAINT fk_Reported_ID FOREIGN KEY (Reported_ID) REFERENCES Member (Member_ID)
)COMMENT = '신고내역';

CREATE TABLE Penalty (
	Penalty_ID	INT AUTO_INCREMENT COMMENT '제재 내역 ID',
	Penalty_duration	DATETIME	NOT NULL COMMENT '제재 일자',
	Penalty_type	VARCHAR(255)	NOT NULL COMMENT '제재 유형',
	Penalty_reason	VARCHAR(255)	NOT NULL COMMENT '제재 사유',
	Penalty_applydate	DATETIME	NOT NULL COMMENT '제재 적용일',
	Penalty_enddate	DATETIME	NOT NULL COMMENT '제재 종료일',
	Member_ID	INT	NOT NULL COMMENT '회원ID',
	CONSTRAINT pk_Penalty_ID PRIMARY KEY (Penalty_ID),
	CONSTRAINT fk_Member_ID_1 FOREIGN KEY (Member_ID) REFERENCES Member (Member_ID)
)COMMENT = '제재내역';


CREATE TABLE Notice (
	Notice_ID 	INT	AUTO_INCREMENT COMMENT '알림ID',
	Notice_type	VARCHAR(255)	NULL COMMENT '알림유형',
	Notice_description	TEXT	NULL COMMENT '알림설명',
   Member_ID	INT	NOT NULL COMMENT '회원ID',
	CONSTRAINT pk_Notice_ID PRIMARY KEY (Notice_ID),
  CONSTRAINT fk_Member_ID_n FOREIGN KEY (Member_ID) REFERENCES Member (Member_ID)
) COMMENT = '알림';


CREATE TABLE Review (
	Review_ID	INT AUTO_INCREMENT COMMENT '리뷰내역ID',
	Review_contents	TEXT	Not NULL COMMENT '리뷰 내용',
	Review_grade	VARCHAR(255)	Not NULL COMMENT '평가 등급',
	Member_ID	INT	NOT NULL COMMENT '회원ID',
  Dealer_ID INT NOT NULL COMMENT '판매자ID',
	CONSTRAINT pk_Review_ID PRIMARY KEY (Review_ID),
	CONSTRAINT fk_Member_ID_3 FOREIGN KEY (Member_ID) REFERENCES Member (Member_ID),
  CONSTRAINT fk_Member_ID_d FOREIGN KEY (Dealer_ID) REFERENCES Member (Member_ID)
)COMMENT = '리뷰내역';


CREATE TABLE Board (
	Board_ID	INT	PRIMARY KEY AUTO_INCREMENT COMMENT '게시판ID',
	Board_type	VARCHAR(255)	NOT NULL COMMENT '게시판 유형',
	Board_description	TEXT	NOT NULL COMMENT '게시판 설명'
) COMMENT = '게시판';

CREATE TABLE Post (
	Post_ID	INT	PRIMARY KEY AUTO_INCREMENT COMMENT '게시물ID',
	Post_title	VARCHAR(255)	NOT NULL COMMENT '게시물 제목',
	Post_contents	TEXT	NOT NULL COMMENT '게시물 내용',
	Post_date	DATETIME	NOT NULL COMMENT '게시물 작성일',
	Post_hits	INT	NOT NULL	DEFAULT 0 COMMENT '조회수',
	Post_last_update	DATETIME	NOT NULL	DEFAULT NOW() COMMENT '마지막 업데이트',
	Post_type	VARCHAR(255)	NOT NULL COMMENT '게시물 유형',
	Deal_date	DATETIME	NULL COMMENT '판매 완료 일자',
	Report_check	TINYINT(1)	NOT NULL	DEFAULT 0 COMMENT '신고 여부',
	Car_ID	INT	NOT NULL COMMENT '차량ID',
	Member_ID	INT	NOT NULL COMMENT '회원 ID',
	Board_ID	INT	NOT NULL COMMENT '게시판ID',
  FOREIGN KEY(Car_ID) References Car(Car_ID),
  FOREIGN KEY(Member_ID) References Member(Member_ID),
  FOREIGN KEY(Board_ID) References Board(Board_ID)
) COMMENT = '게시물';


CREATE TABLE Payment_history (
	Payment_ID	INT	PRIMARY KEY AUTO_INCREMENT COMMENT '결제ID',
	Payment_date	DATETIME	NOT NULL COMMENT '결제일',
	Payment_method	VARCHAR(255)	NOT NULL COMMENT '결제수단',
	Payment_amount	INT	NOT NULL COMMENT '결제금액',
	Car_ID	INT	NOT NULL COMMENT '자동차 ID',
	Member_ID	INT	NOT NULL COMMENT '회원ID',
  FOREIGN KEY(Car_ID) References Car(Car_ID),
  FOREIGN KEY(Member_ID) References Member(Member_ID)
) COMMENT = '결제이력';

CREATE TABLE Interested_car (
	Interested_Car_ID INT AUTO_INCREMENT COMMENT '구매관심차량ID',
	Post_ID INT NOT NULL COMMENT '게시물ID',
	Member_ID INT NOT NULL COMMENT '회원ID',
	Chosen_time DATETIME NOT NULL COMMENT '찜한시간',
	CONSTRAINT PK_INTERESTED_CAR PRIMARY KEY (Interested_Car_ID),
	CONSTRAINT FK_Post_TO_Interested_Car_1 FOREIGN KEY (Post_ID) REFERENCES Post (Post_ID),
	CONSTRAINT FK_Member_TO_Interested_Car_1 FOREIGN KEY (Member_ID) REFERENCES Member (Member_ID)
) COMMENT = '구매관심차량';

CREATE TABLE Reservation (
	Reservation_ID INT AUTO_INCREMENT COMMENT '예약 ID',
	Reservation_status VARCHAR(255) NOT NULL COMMENT '예약상태',
	Reservation_purpose VARCHAR(255) NOT NULL COMMENT '예약목적',
	Reservation_date DATETIME	NOT NULL COMMENT '예약일자',
	Post_ID INT NOT NULL COMMENT '게시물ID',
	Member_ID INT NOT NULL COMMENT '회원ID',
	CONSTRAINT PK_RESERVATION PRIMARY KEY (Reservation_ID),
	CONSTRAINT FK_Post_TO_Reservation_1 FOREIGN KEY (Post_ID) REFERENCES Post (Post_ID),
	CONSTRAINT FK_Member_TO_Reservation_1 FOREIGN KEY (Member_ID) REFERENCES Member (Member_ID)
) COMMENT = '예약내역';

```

</div>
</details>

## 4-테스트

- **TESTCASE Definition Table**

![7 pic](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/152199695/35d855bb-5753-457f-828d-25ca70d49449)

<details>
<summary>TC_001</summary>
	
```sql
TC_001
```

</details>

<details>
<summary>TC_002</summary>
	
```sql
TC_002
```

</details>

<details>
<summary>TC_003</summary>

```sql
TC_003
```

</details>

<details>
<summary>TC_004</summary>

```sql
TC_004
```

</details>

<details>
<summary>TC_005</summary>

```sql
TC_005
```

</details>

<details>
<summary>TC_006</summary>

```sql
TC_006
```

</details>

<details>
<summary>TC_007</summary>

```sql
TC_007
```

</details>

<details>
<summary>TC_008</summary>

```sql
TC_008
```

</details>

<details>
<summary>TC_009</summary>

```sql
TC_009
```

</details>

<details>
<summary>TC_010</summary>

```sql
TC_010
```

</details>








