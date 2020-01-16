쿠버네티스

Basic Norm

Pod - 

Node - 

운영환경에서 컨테이너 관리

* 가동 중지 시간이 없는지 확인
* 다운되면 다른 컨테이너 다시 시작
* 분산 시스템을 탄력적으로 실행
* 애플리케이션의 확장과 장애 조치
* 배포 패턴 제공(카나리아 배포)

기능 

1.  서비스 디스커버리와 로드 밸런싱
2. 스토리지 오케스트레이션
3. 자동화된 롤아웃과 롤백
4. 자동화된 빈 패킹(bin packing)
5. 자동화된 복구(self-healing)
6. 시크릿과 구성 관리

**aaS(as a Service)**

IaaS(Infrastructure as a Service) - EC2, 가상머신

PaaS (Platform as a Service) - 번역 API, 지도 검색 API

SaaS(Software as a Service)- Dropbox과 같은 소프트웨어

Flow

개발  -> 테스트 -> 배포 -> 운영 

Git                       Jenkis    모니터링

컨테이너

Traditional Deployment  

​	리소스 한계 정의 불가능    

​	다른 애플리케이션 성능 저하  

Virtualized Deployment 

​	VM간 애플리케이션 격리

​	일정 수준의 보안성

​	리소스 효율적 활용

Container Deployment

 	격리 속성을 완화

​	