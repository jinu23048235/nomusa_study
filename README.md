# 노무사 노동법 CBT V2

## 기존 GitHub Pages에 업데이트하는 법
1. 기존 학습기록이 필요하면 웹앱의 `데이터 → 학습기록 백업`을 먼저 실행합니다.
2. 이 ZIP을 압축 해제합니다.
3. GitHub의 기존 저장소에서 `Add file → Upload files`를 선택합니다.
4. 압축을 푼 **모든 파일과 폴더**를 업로드합니다. 같은 이름의 파일은 새 버전으로 교체됩니다.
5. 예전 저장소에만 있던 불필요한 파일은 남아 있어도 실행에는 영향이 없지만, 정리하려면 기존 `index.html`, `sw.js`, `manifest.webmanifest`, `icons`를 새 버전으로 교체하고 `assets`, `data` 폴더를 추가하면 됩니다.
6. Commit 후 기존 GitHub Pages 주소를 새로고침합니다.

## 이후 실제 기출 추가법
1. `data/past/2023-32.json`처럼 새 JSON을 추가합니다.
2. `data/catalog.json`의 `past` 배열에 파일 경로·연도·회차를 추가합니다.
3. 오프라인 사용을 위해 `sw.js`의 `FILES`에도 새 JSON 경로를 추가하고 `CACHE` 이름의 숫자를 올립니다.

## 폴더 구조
- `index.html`: 화면 뼈대
- `assets/css/app.css`: 디자인
- `assets/js/app.js`: 채점·필터·오답·통계 로직
- `data/catalog.json`: 데이터 목록
- `data/past/*.json`: 실제 기출
- `data/practice/*.json`: 기출 기반 복습문제
- `sw.js`: 오프라인 캐시

## 주의
V2는 로컬스토리지 키가 새로워 기존 기록을 자동 병합하되, 안전을 위해 기존 버전에서 먼저 백업하는 것을 권장합니다.
