# 🔧 투명 벽에 닿았을 경우 해당 방향으로 가지 못하는 문제

## 🐞 문제
- 플레이어가 투명 벽에 닿으면 특정 방향으로 이동이 불가능해지는 현상

## 🔍 시도한 방법
- Physics Material 2D로 마찰 제거
- 벽의 속도 관련 코드 확인 (없음)

## ✅ 해결 방법
1. 투명 벽에 `Composite Collider 2D` 추가
2. 자동 생성된 `Rigidbody2D`를 `Static`으로 설정
3. `TilemapCollider2D`의 `Used By Composite` 체크
