# 🧐 LG DX School Cx project_Team 3 '원영'_LG ThinQ '오똑이' 서비스
LG DX School 1기에서 2차 CX project 최종 결과물 LG ThinQ '오똑이' 서비스의 구현 코드입니다.

## 🤖 프로젝트 소개
LG전자의 로봇청소기 시장 점유율 확대를 위해 부모님 세대를 대상으로 친절한 '오똑이' 상담사 서비스입니다.

AI 가전 사용이 어려운 부모님 세대가 스스로 사용하실 수 있도록 전문 '오똑이' 상담사가 로봇청소기의 기능 및 LG ThinQ 조작 과정을 교육하고 돕습니다.

## ⏰ 개발 기간 
- 2024.07.24(수) ~ 2024.09.13(금)
- BX 주제 선정
- BX 기획 및 ppt 제작
- BX ~ CX 기획
- 데이터 수집, 분석
- LG 현직자 1,2차 멘토링
- LG 현직자 대상 CX 중간발표
- 서비스 고도화 및 Web App 구현
- CX 최종발표 및 전문 심사위원 평가
  
## 👨‍💻👩‍💻 개발자 소개 
- **이성찬** : 팀장/ 프론트 엔드 개발자 / PM
- **신찬희** : 데이터 분석가/ UX UI Designer
- **이가현** : 데이터 분석가/ UX UI Designer /영상 편집자
- **정다진** : 백앤드 개발자
- **김정섭** :  데이터 분석가/ UX UI Designer

## 🔨 개발환경
- **Version** :  Java 17
- **IDE** : IntelliJ, VS Code
- **Framework** :  SpringBoot 2.7.11
- **ORM** : MongoDB

## 🖥️ 기술 스택
- **Server** : AWS EC2
- **DataBase** :  AWS RDS, Datagrip, JPQL, ERD AqueryTool
- **WS/WAS** : Nginx, Tomcat
- **OCR** : MS Teams, Notion
- **Team meeting** : MS Teams, Notion, Figma

## 🪧 ER Diagram
![dbdiagram.io](https://github.com/user-attachments/assets/d2d352e8-2bec-41a6-9078-63d6aec294e8)

## 📚 Service flow-charts
!['오똑이' flow-charts](https://github.com/user-attachments/assets/2247869c-38e4-48f0-92d4-a644af217e7e)

## 📑 Prototype
![상담사 웹 페이지 프로토타입](https://github.com/user-attachments/assets/1736a1c5-33f7-4b5d-9351-78540c9e9425)
![고객 LG ThinQ '오똑이' 모드 앱 프로토타입](https://github.com/user-attachments/assets/6c2600d8-1f43-4727-9040-fd4000025bb6)

## 📝 프로젝트 아키텍쳐
![프로젝트 아키텍쳐](https://github.com/gmlstjq123/INHA_NET_ZERO_HACKATHON/blob/hello_there-12/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EC%95%84%ED%82%A4%ED%85%8D%EC%B3%90.png)

## 📌 주요 기능
- 오똑이 모드 (상담 교육 모드)
  - 고객이 LG 로봇청소기 사용법을 모를 때 ThinQ 앱 내에 오똑이 모드에서 사용법 상담 및 복습을 할 수 있다.
- 상담하기
   - 고객이 상담을 요청하면 오똑이 상담사와 연결되어 상담 교육을 진행할 수 있다.
   - 상담이 연결되면 고객정보, 고객이 ThinQ 앱에 연동한 로봇청소기의 정보, 해당 로봇청소기의 매뉴얼을 DB에서 조회하여 상담사의 화면에 출력한다.
     - 상담사는 고객과 상담하며 문제를 파악하고 해결방법을 고객에게 step by step으로 교육할 수 있다.
   - 상담 교육을 시작하면 상담사는 고객의 화면을 원격제어할 수 있으며 각 step에 해당하는 목표 버튼을 제외하고 나머지 버튼의 기능을 비활성화한다.
     - 고객이 목표 버튼을 클릭하면 다음 step 화면으로 넘어가며 마지막 step까지 이 과정을 반복한다.
     - 1단계 블러 기능: 고객이 목표 버튼을 클릭하지 못할 때, 상담사가 블러 기능을 활성화하여 목표버튼을 제외한 화면을 어둡게 만들 수 있다.
     - 2단계 블링크 기능: 고객이 1단계 블러 기능으로도 목표 버튼을 클릭하지 못할 때, 상담사가 블링크 기능을 활성화하여 목표버튼 주위에 반짝이는 효과를 줄 수 있다.
     - 3단계 원격제어 기능: 고객이 2단계 블링크 기능으로도 목표 버튼을 클릭하지 못할 때, 상담사가 직접 고객의 화면에서 목표 버튼을 클릭하여 다음 step을 진행할 수 있다.
   - 고객이 마지막 step에 해당하는 목표 버튼을 클릭하면 상담 교육이 완료되며, 상담에 대한 피드백을 별점으로 1점부터 5점까지 남길 수 있다. 별점은 DB에 저장된다.
- 복습하기
  - 상담사는 상담 완료 전 고객에게 상담 내용과 유사한 내용의 복습 노트를 고객의 복습 페이지에 추가할 수 있다. 
  - 고객이 상담 완료 후 복습 페이지에 추가된 복습 노트를 클릭하여 사용법을 복습할 수 있다.
  - 복습 노트를 클릭하면 복습 목표가 표시된다.
  - 복습이 시작되면 첫번째 step부터 마지막 step까지 고객이 스스로 학습하게 되며, 각 step 마다 해당하는 목표 버튼을 제외하고 나머지 버튼의 기능을 비활성화한다.
    - 복습 중 상단에 있는 힌트 버튼을 클릭하면 목표 버튼을 가리키는 손가락이 표시된다.
  - 고객이 마지막 step에 해당하는 목표 버튼을 클릭하면 복습이 완료되며 복습에 대한 피드백을 별점으로 1점부터 5점까지 남길 수 있다. 별점은 DB에 저장된다.
      
## 프론트엔드 기술 구현 과정
**1. DOM 조작과 이벤트 처리**
  - `DOMContentLoaded`: HTML 문서가 완전히 로드된 후 코드를 실행하며 페이지 초기화 작업을 수행
  - 다양한 이벤트(`click`, `mousemove`, `mouseup`, `keydown`, `wheel` 등)를 감지하여 페이지 내에서 발생하는 상호작용을 처리
  - 버튼 클릭 시 오버레이 및 글로우 효과를 토글하거나 해제하며, F8, F9 키를 통해 웹캠 캔버스와 가상 마우스 기능을 토글

**2. WebGL을 통한 그래픽 처리**
  - WebGL을 사용해 사용자의 웹캠 스트림을 `<canvas>`에 렌더링하고, 텍스처로 웹캠 영상을 처리하여 실시간 그래픽을 구현
  - 정점 셰이더와 프래그먼트 셰이더를 작성해 웹캠 프레임의 텍스처 좌표를 계산하고 색상 처리 작업 수행
  - 크로마 키 기능을 통해 프래그먼트 셰이더에서 특정 색상을 감지하고 해당 부분을 투명하게 처리하는 방식 사용

**3. 미디어 처리 (Navigator API 및 MediaPipe)**
  - `getUserMedia API`를 사용해 웹캠에서 실시간 비디오 스트림을 가져와 비디오 요소와 WebGL 캔버스에 연결
  - **MediaPipe Selfie Segmentation**을 사용해 실시간으로 사람과 배경을 구분하고 배경을 투명하게 처리
  - 웹캠 프레임에서 사람을 인식하고 배경을 투명하게 만들어 `<canvas>`에 렌더링

**4. 로컬 스토리지를 활용한 상태 동기화**
  - **localStorage**를 사용해 페이지 간 상태 동기화 및 저장
  - 마우스 위치, 오버레이 및 글로우 상태를 저장하고 이를 다른 페이지나 iframe 간에 동기화
  - 웹캠 재생 시간, 위치, 크기 등의 상태를 저장해 페이지를 새로고침하거나 다른 페이지에서도 상태를 유지

**5. BroadcastChannel을 통한 페이지 간 통신**
  - **BroadcastChannel API**를 사용해 여러 페이지 또는 iframe 간에 메시지를 전송하고 리다이렉션 동기화
  - 페이지 간 특정 버튼 클릭 시 다른 페이지에도 동일한 동작을 수행하도록 동기화
  - 여러 페이지에서 공통된 리다이렉션 상태를 유지하여 일관성 있는 사용자 경험 제공

**6. 동기화된 마우스 움직임과 가상 커서**
  - 가상의 마우스를 표시하고 페이지 간 마우스 움직임을 동기화
  - 마우스가 움직일 때, 로컬 스토리지와 페이지 간 메시지를 통해 다른 페이지에서도 동일한 위치에 가상 마우스를 표시
  - F9 키를 통해 가상 마우스 기능을 켜거나 끌 수 있음

**7. 웹캠 동기화 및 컨트롤**
  - 웹캠 스트림 재생 시간, 위치, 크기 상태를 동기화하여 페이지 간 동일한 웹캠 상태 유지
  - 웹캠 스트림을 드래그 앤 드롭하여 위치를 변경하고, 확대/축소 기능을 지원
  - 페이지 간 웹캠 재생 상태를 동기화하여 일시정지나 재생이 다른 페이지에도 적용

**8. 드래그 앤 드롭과 확대/축소**
  - 웹캠 스트림을 클릭하여 드래그로 위치를 변경할 수 있으며, 마우스 휠을 사용해 비디오 크기를 조절
  - 드래그 및 확대/축소 시 로컬 스토리지를 통해 상태를 저장하고 다른 페이지에서도 동일한 설정을 유지

## ✒️ 백엔드 기술 구현 과정
- API 상세설명 : <https://velog.io/@gmlstjq123/INHA-SW-NET-Zero-%EA%B3%B5%EB%8F%99%ED%95%B4%EC%BB%A4%ED%86%A4-Server-%EC%BD%94%EB%93%9C#3-%ED%92%88%EB%AA%A9%EB%B3%84-%EB%9E%AD%ED%82%B9-%EC%A1%B0%ED%9A%8C>


- API 명세서 : <https://makeus-challenge.notion.site/API-ecafb2a8fb8c427c9e78abf6120d674b>

