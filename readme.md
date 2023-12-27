# Ben-2023

업무소개 및 한해동안 한일들(high-light Low-light), 내년의 주요계획, 개인성장 목표

## 업무소개

### BICScan
블록체인 데이터 정보 조회 서비스

#### 주요 기능
- 특정 지갑 주소, 컨트렉트에 대한 정보 조회
  - 외부 API/ 자체 개발엔진을 사용하여 위험한 지갑 주소인지 점수화
  - 해당 주소가 소유한 다수의 네트워크의 토큰을 모두 조회함

- 사이트 주소를 입력하면 해당 사이트에 관한 정보를 조회함. 특히 악성 Dapp 사이트인지에 대한 정보 제공
  - 외부 API 를 사용하여 조회
  - 사이트 주소의 유사성을 검사해서 피싱사이트 주소인지 확인

- Report 공유 기능


#### highlight 
- 다수 엔진 확보. 자체 개발 엔진. 폭넓은 데이터 제공
- logging system
  - 발생하면 안돼는 오류가 발생하는 경우 개발자가 바로 알 수 있는 알림 시스템을 마련함
  - 오류 알림이 발생하면 바로 대처할 수 있음
  - 오류 로그 뿐만 아니라 특정한 이벤트 발생 등 검색을 쉽게 할 수 있음

#### lowlight 
- 사용자 입장에서 데이터를 이해하기 어려움
  - 각 engine 이 내보내는 데이터에 대한 설명이 부족함
- performance
  - 여러 API 를 호출하고 결과를 취합하는 과정이 매우 느리게 동작
  - 사용자가 API 를 호출하고 기다릴 수 있는 정도를 넘어섬
- 서버관리
  - Dev/Prod EC2 관리 필요(용량/메모리 등)
  - 현재 EC2 시스템이 비용 효율적인지 계산이 필요함

### ABC Web Wallet

#### highlight
- 요구사항 최소화/단시간내 서비스
- AWS Amplify 빌드/배포 과정 단순화
  - AWS amplify 는 repository 와 연결되어 특정 branch 에 작업을 push 하면 해당 branch 가 자동으로 서비스되는 방식
  - 빌드/배포/domain 연결 과정이 매우 단순화 되어있어 개발자가 신경써야될 부분이 거의 없음
- 최신 WebFramework 사용
  - 사용자 경험이 좋은 UI 를 쉽게 개발할 수 있음

#### lowlight
- AWS Amplify 의 스펙을 사전에 숙지하지 못함
  - Amplify 의 backend 는 lambda 기반으로 동작함
  - NextJS 의 UI Streaming feature 를 지원하지 않음
  - UI Streaming 을 사용해서 구현한 page 가 정상적으로 작동하지 않아서 다시 개발함
  - 특정 VPC 내에 속할 수 없음


## 주요계획

### BICScan
- ABC Wallet 2.0 에서 필요한 데이터를 BICScan 에서 제공할 수도 있을 것
  - NFT, Transaction 정보 조회 등
  - 현재 BICScan 은 특정한 사용자가 데이터를 요청하면 해당 데이터를 오랜 시간에 걸쳐 생성하고 제공함
  - ABC Wallet 2.0 에서는 사용자의 요청에 반응해야 하기 때문에 현재 BICScan 의 구조와 잘 맞지 않음
- NFT/Transaction/자산 정보 조회
  - 사용자의 요청에 빠르게 제공할 수 있는 방안을 강구해야 함


### Web Wallet / WaaS
- Serverless 도입
- E2E 테스트 도입


## 개인성장 목표 

### AWS Certified Developer – Associate 취득
- AWS architecture 에 대한 모범사례에 대한 지식&이해 습득할 수 있음
- AWS cloud 기반 애플리케이션의 개발,배포,디버깅 에 능숙해야 함

### 프로그래밍 언어 go/rust
- 다른 프로그래밍 언어로 개발할 떄 더 좋은 개발자가 될 수 있다고 생각함
- 같은 기능을 구현하더라도 언어마다 다른 접근 방식을 사용하기 때문에, 기존에 다른 언어로 작성한 코드/데이터를 다른 방식으로 생각하게 됨
  - 예를들어 어떤 언어는 데이터를 특정한 방식으로 다루게 강제하는데, 이유를 이해하면 다른 언어로 개발을 할 때도 해당 접근방식에 대해 생각하게 됨

### Auto scaling / Serverless
- Serverless 로 운영하는 것이 비용적 측면에서 유리할 수 있음
  - 현재 (Serverless 를 사용하지 않는) 서버가 대부분의 시간을 유휴 상태로 보내고 있을 수 있음. 이런 시간으로 확인해보고 Serverless 를 도입하면 비용 절감 가능
  - 유동적으로 자원을 사용할 수 있음(auto scaling)
- Serverless 는 유지보수가 필요하지 않음. 원래 업무에 더 집중할 수 있음
- Serverless 를 꺼리게 되는 이유
  - 새로운 것을 시도하는 것에 대한 두려움. 공부를 더 해야 함

### Blockchain Indexer 개발
- blockchain 데이터를 검색할 수 있는 서비스
- 요구사항 정리, 데이터 저장 방법 등을 고민 해야 함
  - transaction 발생 통지
  - 특정 주소/다수의 주소 의 총 자산 내역 조회
- 요구사항에 필요한 데이터만 담는 경우 검색 performance, 데이터 크기 등 
