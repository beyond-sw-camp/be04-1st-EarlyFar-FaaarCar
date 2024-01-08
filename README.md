# be04-1st-EarlyFar-FaaarCar
얼리멀리(Early&amp;Far) 3조입니다.

---

# 제안요청서

# 1. 프로젝트 개요

멀리카아 프로젝트는 급격하게 성장 하는 중고차 시장에서 발생하는 수많은 거래와 정보를 데이터베이스로 구축하여 다양한 정보를 체계적으로 관리하고 활용하는데 그 목적이 있습니다. 프로젝트의 추진배경은 다음과 같습니다.

## 1-1 필요성

한국 국토교통부 데이터 통합 채널에서 제공한 ‘자동차등록현황보고’ 통계에 따르면 전국적으로 자동차등록현황은 2010년을 기준으로 10년 동안 자동차에 대한 수요는 계속해서 증가하고 있다. 또한 국내 거대 규모 중고차 거래 플랫폼 중 하나인 KB차차차의 중고차 매물건수는 론칭했던 2016년 기준 15,247대에서 2018년에는 100,000대가 돌파되면서 2년 만에 8배 이상의 중고차 매물이 늘어 나는 것이 확인되었다. 결과적으로 중고차 시장의 급격한 성장으로 인해서, 수많은은 거래 및 정보가 생성되고 있고 이에 따라 중고차 관련 정보를 체계적으로 관리하여 금융 프로세스를 향상시킬 필요성이 생겼습니다.

![1 pic](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/101622086/eb73a9cb-412a-4cba-b16a-3fc0d82d9599)
                                  *사진 1:자동차등록현황 및 이륜차신고현황*

![2 pic](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/101622086/5769231a-a2c6-4485-8a4a-08540a48f0e0)
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

![3 pic](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/101622086/5cf354ca-6931-4f50-9870-a873e4b3abd4)

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

[farcar.damx](https://prod-files-secure.s3.us-west-2.amazonaws.com/c78cddc1-c25c-4915-ab0f-e94172746e8b/e546da64-df5c-4bc3-9e98-9f67627776b6/farcar.damx)

![4 pic](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/101622086/a2d0b223-d35c-4a91-b17f-ad798da0dd53)

개념 모델링

![5 pic](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/101622086/5244fae5-ee7e-4072-8042-3a3a0b6b4a8b)

DA# 논리 모델

## 3-3 물리 모델링

![6 pic](https://github.com/beyond-sw-camp/be04-1st-EarlyFar-FaaarCar/assets/101622086/679900b8-54d8-4b47-b1ce-21b515c14e0d)

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
    
    CREATE TABLE Accident (
    	Accident_code VARCHAR(255) NOT NULL COMMENT '사고  코드',
    	Accident_type VARCHAR(255) NOT NULL COMMENT '사고 유형',
    	Accident_description TEXT NOT NULL COMMENT '사고 유형 설명',
    	CONSTRAINT PK_ACCIDENT PRIMARY KEY (Accident_code)
    )COMMENT = '사고';
    
    CREATE TABLE Accident_History (
    	Accident_ID INT AUTO_INCREMENT COMMENT '차동자 사고 ID',
    	Accident_damage_degree INT NOT NULL COMMENT '피해정도',
    	Accident_date DATETIME NOT NULL COMMENT '발생 일자',
    	Insurance_claim_check TINYINT(1) NOT NULL DEFAULT 0 COMMENT '보험청구여부',
    	Accident_code VARCHAR(255) NOT NULL COMMENT '사고  코드',
    	Car_ID INT NOT NULL COMMENT '자동차 ID',
    	CONSTRAINT PK_ACCIDENT_HISTORY PRIMARY KEY (Accident_ID),
    	CONSTRAINT FK_Accident_TO_Accident_History_1 FOREIGN KEY (Accident_code) REFERENCES Accident (Accident_code),
    	CONSTRAINT FK_Inspection_record_TO_Accident_History_1 FOREIGN KEY (Car_ID) REFERENCES Car (Car_ID)
    )COMMENT = '자동차침수이력';
    
    CREATE TABLE Inundation (
    	Inundation_ID INT	AUTO_INCREMENT COMMENT '차동자 침수 ID',
    	Inundation_degree INT NOT NULL COMMENT '침수정도',
    	Inundation_date DATETIME NOT NULL COMMENT '발생 일자',
    	Accident_code VARCHAR(255)	NOT NULL COMMENT '사고  코드',
    	Car_ID INT NOT NULL COMMENT '자동차 ID',
    	CONSTRAINT PK_INUNDATION PRIMARY KEY (Inundation_ID),
    	CONSTRAINT FK_Accident_TO_Inundation_1 FOREIGN KEY (Accident_code) REFERENCES Accident (Accident_code),
    	CONSTRAINT FK_Inspection_record_TO_Inundation_1 FOREIGN KEY (Car_ID) REFERENCES Car (Car_ID)
    )COMMENT = '자동차침수이력';
    
    CREATE TABLE USER (
    	User_ID	INT	PRIMARY KEY AUTO_INCREMENT COMMENT '회원ID',
    	User_name	VARCHAR(255)	NOT NULL COMMENT '이름',
    	User_nickname	VARCHAR(255)	NOT NULL COMMENT '닉네임',
    	User_password	VARCHAR(255)	NOT NULL COMMENT '비밀번호',
    	User_email	VARCHAR(255)	NOT NULL COMMENT '이메일',
    	User_phoneNum	VARCHAR(255)	NOT NULL COMMENT '전화번호',
    	User_address	VARCHAR(255)	NOT NULL COMMENT '주소',
    	User_birth	DATETIME	NOT NULL COMMENT '생년월일',
    	User_sign_up_date	DATETIME	NOT NULL COMMENT '가입일',
    	User_coupon	INT	NULL	DEFAULT 0 COMMENT '보유 쿠폰',
    	Dealer_company	VARCHAR(255)	NULL COMMENT '딜러 회사명',
    	Dealer_region	VARCHAR(255)	NULL COMMENT '딜러 근무지',
    	Dealer_grade	INT	NULL COMMENT '딜러 등급',
    	User_type	INT	NOT NULL COMMENT '회원 유형',
    	User_blacklist	TINYINT(1)	NULL	DEFAULT 0 COMMENT '블랙회원여부',
    	Restriction_date	DATETIME	NULL COMMENT '제재 적용일',
    	Restriction_end_date	DATETIME	NULL COMMENT '제재 종료일',
    	Login_fail_stack	INT	NULL DEFAULT 0 COMMENT '로그인실패횟수',
    	Report_issue_stack	INT	NULL DEFAULT 0 COMMENT '누적신고횟수',
    	Login_restriction_check	TINYINT(1)	NULL	DEFAULT 0 COMMENT '접근제한여부',
    	User_withdraw_check	TINYINT(1)	NULL	DEFAULT 0 COMMENT '탈퇴여부',
    	User_withdraw_date DATE NULL COMMENT '탈퇴날짜'
    )COMMENT = '회원';
    
    CREATE TABLE Coupon (
    	Coupon_number INT AUTO_INCREMENT COMMENT '쿠폰 번호',
    	Coupon_date DATETIME NOT NULL COMMENT '발급 일자',
    	Coupon_usage_status TINYINT(1) NOT NULL DEFAULT 0 COMMENT '쿠폰 사용 상태',
    	Coupon_description TEXT NOT NULL COMMENT '쿠폰 설명',
    	User_ID INT NOT NULL COMMENT '회원ID',
    	CONSTRAINT PK_COUPON PRIMARY KEY (Coupon_number),
    	CONSTRAINT FK_User_TO_Coupon_1 FOREIGN KEY (User_ID) REFERENCES User (User_ID)
    )COMMENT = '쿠폰';
    
    CREATE TABLE Login_log (
    	Login_log_ID	INT AUTO_INCREMENT COMMENT '로그인내역ID',
    	Success_check	TINYINT(1)	NOT NULL	DEFAULT 0 COMMENT '성공여부',
    	Attempt_date	DATE	NOT NULL COMMENT '시도날짜',
    	Attempt_time	TIME	NOT NULL COMMENT '시도시간',
    	Attempt_region	VARCHAR(255)	NOT NULL COMMENT '시도위치',
    	User_ID	INT	NOT NULL COMMENT '회원ID',
    	CONSTRAINT pk_Login_log_ID PRIMARY KEY (Login_log_ID),
    	CONSTRAINT fk_User_ID FOREIGN KEY (User_ID) REFERENCES User (User_ID)
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
      CONSTRAINT fk_Reporter_ID FOREIGN KEY (Reporter_ID) REFERENCES User (User_ID),
    	CONSTRAINT fk_Reported_ID FOREIGN KEY (Reported_ID) REFERENCES User (User_ID)
    )COMMENT = '신고내역';
    
    CREATE TABLE Penalty (
    	Penalty_ID	INT AUTO_INCREMENT COMMENT '제재 내역 ID',
    	Penalty_duration	DATETIME	NOT NULL COMMENT '제재 일자',
    	Penalty_type	VARCHAR(255)	NOT NULL COMMENT '제재 유형',
    	Penalty_reason	VARCHAR(255)	NOT NULL COMMENT '제재 사유',
    	Penalty_applydate	DATETIME	NOT NULL COMMENT '제재 적용일',
    	Penalty_enddate	DATETIME	NOT NULL COMMENT '제재 종료일',
    	User_ID	INT	NOT NULL COMMENT '회원ID',
    	CONSTRAINT pk_Penalty_ID PRIMARY KEY (Penalty_ID),
    	CONSTRAINT fk_User_ID_1 FOREIGN KEY (User_ID) REFERENCES User (User_ID)
    )COMMENT = '제재내역';
    
    CREATE TABLE Notice (
    	Notice_ID 	INT	AUTO_INCREMENT COMMENT '알림ID',
    	Notice_type	VARCHAR(255)	NULL COMMENT '알림유형',
    	Notice_description	TEXT	NULL COMMENT '알림설명',
       User_ID	INT	NOT NULL COMMENT '회원ID',
    	CONSTRAINT pk_Notice_ID PRIMARY KEY (Notice_ID),
      CONSTRAINT fk_User_ID_n FOREIGN KEY (User_ID) REFERENCES User (User_ID)
    ) COMMENT = '알림';
    
    CREATE TABLE Review (
    	Review_ID	INT AUTO_INCREMENT COMMENT '리뷰내역ID',
    	Review_contents	TEXT	Not NULL COMMENT '리뷰 내용',
    	Review_grade	VARCHAR(255)	Not NULL COMMENT '평가 등급',
    	User_ID	INT	NOT NULL COMMENT '회원ID',
      Dealer_ID INT NOT NULL COMMENT '판매자ID',
    	CONSTRAINT pk_Review_ID PRIMARY KEY (Review_ID),
    	CONSTRAINT fk_User_ID_3 FOREIGN KEY (User_ID) REFERENCES User (User_ID),
      CONSTRAINT fk_User_ID_d FOREIGN KEY (Dealer_ID) REFERENCES User (User_ID)
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
    	User_ID	INT	NOT NULL COMMENT '회원 ID',
    	Board_ID	INT	NOT NULL COMMENT '게시판ID',
      FOREIGN KEY(Car_ID) References Car(Car_ID),
      FOREIGN KEY(User_ID) References User(User_ID),
      FOREIGN KEY(Board_ID) References Board(Board_ID)
    ) COMMENT = '게시물';
    
    CREATE TABLE Payment_History (
    	Payment_ID	INT	PRIMARY KEY AUTO_INCREMENT COMMENT '결제ID',
    	Payment_date	DATETIME	NOT NULL COMMENT '결제일',
    	Payment_method	VARCHAR(255)	NOT NULL COMMENT '결제수단',
    	Payment_amount	INT	NOT NULL COMMENT '결제금액',
    	Car_ID	INT	NOT NULL COMMENT '자동차 ID',
    	User_ID	INT	NOT NULL COMMENT '회원ID',
      FOREIGN KEY(Car_ID) References Car(Car_ID),
      FOREIGN KEY(User_ID) References User(User_ID)
    ) COMMENT = '결제이력';
    
    CREATE TABLE Interested_Car (
    	Interested_Car_ID INT AUTO_INCREMENT COMMENT '구매관심차량ID',
    	Post_ID INT NOT NULL COMMENT '게시물ID',
    	User_ID INT NOT NULL COMMENT '회원ID',
    	Chosen_time DATETIME NOT NULL COMMENT '찜한시간',
    	CONSTRAINT PK_INTERESTED_CAR PRIMARY KEY (Interested_Car_ID),
    	CONSTRAINT FK_Post_TO_Interested_Car_1 FOREIGN KEY (Post_ID) REFERENCES Post (Post_ID),
    	CONSTRAINT FK_User_TO_Interested_Car_1 FOREIGN KEY (User_ID) REFERENCES User (User_ID)
    ) COMMENT = '구매관심차량';
    
    CREATE TABLE Reservation (
    	Reservation_ID INT AUTO_INCREMENT COMMENT '예약 ID',
    	Reservation_status VARCHAR(255) NOT NULL COMMENT '예약상태',
    	Reservation_purpose VARCHAR(255) NOT NULL COMMENT '예약목적',
    	Reservation_date DATETIME	NOT NULL COMMENT '예약일자',
    	Post_ID INT NOT NULL COMMENT '게시물ID',
    	User_ID INT NOT NULL COMMENT '회원ID',
    	CONSTRAINT PK_RESERVATION PRIMARY KEY (Reservation_ID),
    	CONSTRAINT FK_Post_TO_Reservation_1 FOREIGN KEY (Post_ID) REFERENCES Post (Post_ID),
    	CONSTRAINT FK_User_TO_Reservation_1 FOREIGN KEY (User_ID) REFERENCES User (User_ID)
    ) COMMENT = '예약내역';
    ```

</div>
</details>

## 4-테스트

- **TESTCASE**
    
    
    | TC_ID | REQ_ID | 대분류 | 중분류 | 소분류 | 사전 조건 | 실행 순서 | 기대 결과 | 테스트 결과(pass/fail) | 비고 |
    | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
    | TC_001 | REQ001 | 회원 | 회원 가입 | 회원 가입 | 1. 회원 테이블에 해당 회원 정보가 없음 | 1. 회원 가입 시 입력 된 정보를 회원(User)  테이블에 저장 | 입력된 회원 정보가 회원 테이블에 저장된다. | pass | insert |
    | TC_002 | REQ002 | 회원 | 회원 탈퇴 | 회원 탈퇴 | 1. 회원 로그인 된 상태
    2. 회원 테이블에 해당 회원 정보 있음 | 1. 탈퇴 요청한 회원의 정보를 삭제 | 탈퇴 회원의 탈퇴 여부와 탈퇴 날짜가 업데이트된다. | pass | update |
    | TC_003 | REQ003 | 회원 | 로그인 | 로그인 성공 | 1. 회원 테이블에 회원 정보 있음
    2. 로그인 성공 | 1. 로그인 성공한 회원의 로그인 내역 저장 | 로그인 성공한 회원의 로그인 내역 테이블에 내역이 저장된다. | pass | insert |
    | TC_004 | REQ003 | 회원 | 로그인 | 로그인 실패 | 1. 회원 테이블에 회원 정보 있음
    2. 로그인 실패 | 1. 로그인 실패한 회원의 로그인 내역 저장
    2. 회원 테이블의 로그인 실패 횟수 업데이트 | 로그인 실패한 회원의 로그인 내역이 저장되고 로그인 실패 횟수가 업데이트된다. | pass | Trigger
    (insert&update)  |
    | TC_005 | REQ005 | 회원 | 회원 정보 | 비밀번호 재설정 | 1. 회원 로그인 된 상태
    2. 회원 테이블에 해당 회원 정보가 있음 | 1. 해당 회원의 비밀번호 변경 | 해당 회원의 비밀번호가 업데이트된다. | pass | update |
    | TC_006 | REQ006 | 회원 | 회원 정보 | 프로필 수정 | 1. 회원 로그인 된 상태
    2. 회원 테이블에 해당 회원 정보가 있음 | 1. 해당 회원의 닉네임, 이메일, 전화번호, 주소 등의 프로필 정보 수정 | 해당 회원의 프로필 정보가 업데이트된다. | pass | update |
    | TC_007 | REQ014 | 회원 | 회원 정보 | 평가 및 리뷰 | 1. 회원 로그인 된 상태
    2. 해당 회원의 리뷰 내역 존재  | 1. 현재 사용자의 리뷰 내역 조회 | 해당 회원의 리뷰 내역이 조회된다. | pass | select (JOIN)  |
    | TC_008 | REQ017 | 자동차 | 자동차 정보 | 자동차 등록 | 1. 등록하고자 하는 차량의 정보가 중복되지 않아야함. | 1. 등록하고자 하는 차량 정보를 자동차(Car) 테이블에 저장
    2. 해당 차량의 소유 이력을 소유 이력 테이블에 저장
    3. 해당 차량의 사고 이력을 자동차 사고 이력 테이블에 저장
    4. 해당 차량의 침수 이력을 자동차 침수 이력 테이블에 저장 | 등록하고자 하는 자동차의 정보가 자동차 정보 관련 테이블들에 정상적으로 저장된다. | pass | Transaction
     |
    | TC_009 | REQ040 | 회원 | 회원 신고 | 제재일 업데이트 및 회원 계정 비활성화 (강제탈퇴) | 기존의 누적 신고 횟수가 5회 이상 또는 30회 이상인 회원 | 1.누적신고횟수가 5배수인 (ex 5, 10, …30) 회원이 존재 한다는 가정하에 (User) 테이블 인스턴스 생성
    2. 누적 횟수가 5회에 도달하면 회원은 블랙리스트  인스턴스가 활성화 (’1’) 및 횟수가 변경된 날짜 기준으로 제재 기간이 적용
    3. 만약 누적신고횟수가 30이 넘어가면 회원탈퇴여부를 업데이트 (’1’) | 블랙리스트로 지정된 회원을 구분할 수 있게 되며, 해당 회원에게 제재날짜와 탈퇴여부를 결정할 수 있다. | pass | Trigger
    (Update) |
    | TC_010 | REQ023 | 자동차 | 자동차 정보 | 자동차 정보 조회 | 1. 자동차가 등록된 상태 | 1. 등록된 자동차 정보와 해당 자동차와 관련된 정보들을 조회 | 조회하고자 하는 자동차와 관련 정보들이 조회된다. | pass | view 
    (Multi JOIN) |
    
    - 결과
    1. **TC_001**
    
    ```sql
    INSERT INTO User (
    	User_ID, User_name, User_nickname, User_password, User_email, User_phoneNum, User_address, User_birth,
    	User_sign_up_date, User_coupon, Dealer_company, Dealer_region, Dealer_grade, User_type, User_blacklist,
    	Restriction_date, Restriction_end_date, Login_fail_stack, Report_issue_stack, Login_restriction_check,
    	User_withdraw_check, User_withdraw_date 
    )
    VALUES 
    (
     NULL, 
     'test','test_nick','test_passwd','test@gmail.com','010-5678-1234','서울','2023-1-1 00:00:00', NOW(),
      NULL,	'test_company',	 'test_region',  1,	1,	NULL,	NULL,	NULL,	NULL,	NULL,	NULL, 0,	NULL 
    );
    ```
    
    1.  TC**002**
    
    ```sql
    update User set User_withdraw_check=1, User_withdraw_date=NOW() WHERE user_id = 4;
    ```
    
    1. **TC_003**
    
    ```sql
    INSERT INTO Login_log (Success_check, Attempt_date, Attempt_time, Attempt_region, User_ID) Values (1, NOW(), NOW(), '서울', 1);
    ```
    
    1. **TC_004**
    
    ```sql
    DELIMITER //
    
    CREATE OR REPLACE TRIGGER LOGIN_FAIL_TR
        AFTER INSERT 
        ON Login_log
        FOR EACH ROW
    BEGIN 
        IF NEW.Success_check = 0 THEN
            UPDATE USER
            SET Login_fail_stack = Login_fail_stack + 1
            WHERE user_id = New.user_id; 
        END IF;
    END//
    
    DELIMITER ;
    ```
    
    1. **TC_005**
    
    ```sql
    update User set user_password='updatetest' WHERE User_id = 5;
    ```
    
    1. **TC_006**
    
    ```sql
    update User set user_nickname='testnickname', user_email='updatetest@gmail.com', user_phonenum='010-8888-8888', user_address='광주' WHERE User_id = 5;
    ```
    
    1. **TC_007**
    
    ```sql
    SELECT b.user_name, a.review_grade, a.review_contents 
      FROM review a
      JOIN User b ON a.dealer_id = b.user_id
     WHERE a.dealer_id = 2;
    ```
    
    1. **TC_008**
    
    ```sql
    -- Transaction 시작
    START TRANSACTION;
    
    -- 예시: 자동차 정보 삽입
    INSERT INTO Car (
    	  Car_ID, Car_field, Car_model, Car_year, Car_mileage, Car_condition, 
    	  Car_transmission, Car_oiltype, Car_engine, Car_fuel_efficiency,
    	  Accident_check, Inundation_check, Selling_price, Picture_URL, 
    	  Picture_origin, Picture_rename, Model_ID, Insepction_record_URL
    )
    VALUES 
    (
    	 99, 'Hyundai', 'Sonata', 2019, 50000, 'Good', 'Automatic', 
    	 'Gasoline', '2.0L', 15, 0, 0, 20000, '/images/sonata.jpg', 
    	 'sonata_original.jpg', 'sonata_rename.jpg', 'M2', '/inspection/M2'
    );
    
    -- 다른 테이블에도 삽입 또는 업데이트 등 필요한 작업 수행
    -- Ownership_history insert
    INSERT INTO Ownership_history (
        Previous_Owner, Current_Owner, Ownership_start, Ownership_end, 
    		Reason_transfer, Descript_transfer, Car_ID
    )
    VALUES 
    (
        '이재원', '이준형', '2021-04-03 09:00:00', '2023-03-15 17:30:00',
        '직장 지역이동에 의한 판매', '차량 상태 우수, 주행거리 낮음', 99
    );
    
    -- Accident_History insert
    SELECT * FROM Accident_History;
    INSERT INTO Accident_History (
        Accident_damage_degree, Accident_date, Insurance_claim_check,
        Accident_code, Car_ID
    )
    VALUES 
    (
        2, '2022-05-20 16:00:00',  1,
        'FACD001', 99
    );
    
    -- Inundation insert
    SELECT * from Inundation;
    INSERT INTO Inundation (
        Inundation_degree, Inundation_date, Accident_code, Car_ID
    )
    VALUES 
    (
        3, '2022-07-10 10:15:00', 'DACD001', 99
    );
    
    -- Transaction 종료
    COMMIT;
    ```
    
    1. **TC_009**
    
    ```sql
    -- User 테이블에 대한 Trigger 정의
    DELIMITER //
    CREATE TRIGGER AfterReportUpdate
    BEFORE UPDATE ON User
    FOR EACH ROW
    BEGIN
      -- 누적신고횟수가 5의 배수일 때 제재 적용
      IF NEW.Report_issue_stack % 5 = 0 AND NEW.Report_issue_stack < 30 THEN
        SET NEW.User_blacklist = 1;
        SET NEW.Restriction_date = NOW();
        SET NEW.Restriction_end_date = DATE_ADD(NOW(), INTERVAL NEW.Report_issue_stack DAY);
      END IF;
    
      -- 누적신고횟수가 30이 넘어가면 회원의 회원탈퇴 여부가 1(탈퇴)로 업데이트
      IF NEW.Report_issue_stack >= 30 THEN
     		SET NEW.User_withdraw_check = 1;
     		SET NEW.User_withdraw_date = NOW();
      END IF;
    END;
    //
    DELIMITER ;
    ```
    
    ```sql
    
    -- Trigger 적용 확인
    SELECT * FROM user;
    INSERT INTO User (
    	User_ID, User_name, User_nickname, User_password, User_email, User_phoneNum,
    	User_address, User_birth, User_sign_up_date, User_coupon, Dealer_company,
    	Dealer_region, Dealer_grade, User_type, User_blacklist, Restriction_date, Restriction_end_date,
    	Login_fail_stack, Report_issue_stack, Login_restriction_check, User_withdraw_check,
    	User_withdraw_date 
    )
    VALUES 
    (
     99, 
     '홍길동',
     '회원닉네임이영',
     'qlalfqjsgh1234',
     'hongmail@daum.net',
     '010-2222-5555',
     '부산',
     '1993-1-3 00:00:00',
      NOW(),
      NULL,	-- 보유쿠폰
      NULL,	
      NULL,  
      NULL,	-- 딜러등급
      0,	-- 회원유형 1=판매자 0=구매자
      NULL,	-- 블랙 여부
      NULL,	-- 제재 시작일
      NULL,	-- 제재 종료일
      NULL,	-- 로그인 실패 횟수
      4,	-- 누적 신고 횟수
      NULL,	-- 로그인 제한 여부
      0,	-- 탈퇴여부
      NULL -- 탈퇴날짜
    ),
    (
     100, 
     '홍구구',
     '회원닉네임이영',
     'qlalfqjsgh1234',
     'hongmail@daum.net',
     '010-2222-5555',
     '대구',
     '1996-1-3 00:00:00',
      NOW(),
      NULL,	-- 보유쿠폰
      NULL,	
      NULL,  
      NULL,	-- 딜러등급
      0,	-- 회원유형 1=판매자 0=구매자
      1,	-- 블랙 여부
      '2023-12-1 00:00:00',	-- 제재 시작일
      '2023-12-26 00:00:00',	-- 제재 종료일
      NULL,	-- 로그인 실패 횟수
      28,	-- 누적 신고 횟수
      NULL,	-- 로그인 제한 여부
      0,	-- 탈퇴여부
      NULL -- 탈퇴날짜
    );
    SELECT * FROM user;
    UPDATE user SET report_issue_stack = report_issue_stack + 1 WHERE User_ID IN (99, 100);
    SELECT * FROM USER;
    UPDATE user SET report_issue_stack = report_issue_stack + 5 WHERE User_ID IN (99, 100);
    SELECT * FROM USER;
    ```
    
    1. **TC_010**
    
    ```sql
    -- 이중 Join을 활용한 View 생성
    CREATE VIEW CarOwnershipView AS
    SELECT Car.Car_ID, Car.Car_model, Model.Model_name, Ownership_history.Current_Owner
    FROM Car
    JOIN Model ON Car.Model_ID = Model.Model_ID
    JOIN Ownership_history ON Car.Car_ID = Ownership_history.Car_ID;
    SELECT * FROM CarOwnershipView;cd 
    ```