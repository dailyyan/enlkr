# Seoul Anomaly ENL · 2026.08.22

2026년 8월 22일 토요일 서울에서 열리는 XM Anomaly의 Enlightened 진영 비공식 팬 홍보 사이트입니다.

> Fan-operated. Not affiliated with Niantic, Inc.
> Ingress 및 Enlightened 로고는 Niantic, Inc.의 재산입니다.

---

## 📂 구조

```
.
├── docs/                 ← GitHub Pages 배포 폴더 (Settings → Pages 에서 이 경로 지정)
│   ├── index.html        ← 한국어 홈
│   ├── ja/index.html     ← 일본어 홈
│   ├── assets/
│   │   ├── styles.css
│   │   ├── seoul-night.png
│   │   └── enl-logo.png
│   └── README.md
│
└── (그 외 파일들은 디자인 작업용 React/Babel 시안 — 배포 불필요)
```

## 🚀 GitHub Pages 배포

1. 이 폴더를 신규 리포에 푸시합니다.
2. 리포 **Settings → Pages**.
3. **Source: Deploy from a branch**, **Branch: `main` / `/docs`** 선택, Save.
4. 1분 뒤 `https://<USERNAME>.github.io/<REPO>/` 에서 접속 가능합니다.

### 로컬에서 미리보기

`docs/` 폴더에서 정적 서버 하나만 띄우면 됩니다.

```bash
cd docs
python3 -m http.server 8000
# → http://localhost:8000
```

## ✏️ 콘텐츠 수정 가이드

- **카운트다운 목표 시각**: `docs/index.html`, `docs/ja/index.html` 하단 `<script>`의 `new Date("2026-08-22T13:00:00+09:00")` 값을 수정.
- **등록 링크**: 두 파일에서 `href="#"`로 비워둔 `ENL 등록하기` / `参加登録する` 버튼의 href를 실제 링크로 교체.
- **그린 톤 변경**: `docs/assets/styles.css` 상단 `--enl: #00c04a;` 값만 바꾸면 전 페이지 일괄 적용.
- **새 이미지**: `docs/assets/` 에 PNG/JPG 넣고 HTML에서 경로만 교체.

## 📐 디자인 작업 (별도)

프로젝트 루트의 `Seoul Anomaly ENL - Home Mockups.html` 은 React 기반 디자인 작업 캔버스로, 변형을 비교하고 색조를 토글해보기 위한 도구입니다. GitHub Pages 에 배포할 필요 없습니다.
