# 🔧 오브젝트 풀링 및 보스 스킬 반환 문제

## 🐞 문제
- 보스 사망 후에도 스킬 오브젝트가 씬에 남아 있음

## 🔍 시도한 것
- 스킬 오브젝트를 리스트로 저장 후 보스 사망 시 `ReturnToPool()` 호출
- 생성 위치를 빈 오브젝트 아래로 이동
- 디버깅을 통해 리스트와 반환 로직 점검

## ⚠️ 추가 발생 오류
- `KeyNotFoundException: The given key 'Untagged' was not present in the dictionary`

## 🔧 원인
- Unity 태그와 풀링 시스템에서 사용하는 태그 기준이 다름

## ✅ 해결 방법
- 각 스킬 오브젝트에 `PoolTag` 컴포넌트 추가
- 생성 시 `poolTag` 속성 저장 → 반환 시 해당 태그로 딕셔너리 접근
