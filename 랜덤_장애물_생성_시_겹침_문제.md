# 🔧 랜덤 장애물 생성 시 겹침 문제

## 🐞 문제
- 장애물이 랜덤 배치될 때 서로 겹쳐 생성되는 현상 발생

## 🔍 시도한 것
- `Physics2D.OverlapBox()` 사용
- `Vector2.Distance()`로 거리 체크
- 장애물 위치 설정 로직을 `ObstacleController` → `MapController`로 이동

## ✅ 해결 방법
- 위치 배치 조건을 두 가지로 설정:
  1. `OverlapBox()`로 충돌 검사
  2. `Vector2.Distance()`로 기존 장애물과 거리 검사
