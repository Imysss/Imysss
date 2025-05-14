# 🔧 슈팅 중 화면 버벅임

## 🐞 문제
- 화살의 유도기능 활성화 상태에서 화살 개수가 10개 이상일 경우 화면 버벅임 발생

## 🔍 원인
- 화살에 부착된 `ChaseMonster` 스크립트의 `OnTriggerEnter2D()`가 
  모든 오브젝트를 대상으로 `CompareTag("Monster")` 호출

## ✅ 해결 방법
- Unity > Project Settings > Physics 2D 설정에서 
  `Weapon` 레이어가 `Monster` 레이어만 충돌하도록 설정
