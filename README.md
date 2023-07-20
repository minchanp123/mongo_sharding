## 수집데이터 적재용 MongoDB 작업 및 설계

### 담당 업무

   - MongoDB 샤딩 구축 및 운용
   - db 확장성을, 비용 절감을 위해 샤딩으로 작업
   - 클라우드 서버에 사용 (AWS EC2, Azure VM)
   - 수집 데이터 스토리지용으로 사용

### 샤딩 구조

#### router 
   - primary, secondary의 레플리카 셋의 중개자 역할
   - 전체 노드의 쿼리 기능
    
#### config
   - data chank위치 정보 저장

#### primary
   - 메인 스토리지 db서버

#### secondary
   - 서브 스토리지 db서버
   - 복구/백업용

#### arbiter
   - primary가 죽을 경우 secondary를 primary로 승격 해주는 역할


### 샤딩 방법
   - MongoDB 샤딩 메뉴얼.docx 참고
