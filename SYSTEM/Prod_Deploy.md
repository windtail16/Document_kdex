운영서버 배포 과정 정리
=====================

1. dexko.co.kr, api.dexko.co.kr, io.dexko.co.kr 도메인 변경 => 
2. DB 변경
3. v1-스테이지 서버에 배포 (Front, WAS, Trade, Wallet-Api, WebSocket, BackOffice)
4. v1-스테이지 테스트
5. 테스트 완료
6. 운영서버 배포 (Front, WAS, Wallet-Api) : Trade, WebSocket, BackOffice는 스테이지가 곧 운영
7. api.dexko.co.kr, io.dexko.co.kr 도메인 변경
8. api, io 서버 도메인 변경 확인 후 dexko.co.kr 도메인 변경

### 유의 사항
1. 거래 테스트시 일반유저가 걸어놓은 매수, 매도 건을 체결시키면 안됨.
2. 거래 테스트시 호가 변동이 있으면 안됨.
3. 만약 해야 한다면 테스트 후 롤백 기능이 추가 되어야 함.