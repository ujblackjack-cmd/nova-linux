# nova-linux
# 🌐 NOVA Portal

> 개인 서버에 배포하는 미니멀 다크 테마 포털 사이트

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)

---

## ✨ 기능

| 기능 | 설명 |
|------|------|
| 🕐 실시간 시계 | 초 단위 업데이트 디지털 시계 |
| 🔍 통합 검색 | Google / Naver / YouTube / GitHub 전환 검색 |
| 🌤 날씨 위젯 | Open-Meteo API 기반 실시간 날씨 (API 키 불필요) |
| 🔗 빠른 링크 | 자주 쓰는 사이트 바로가기 8개 |
| 📰 헤드라인 | 뉴스 링크 모음 |
| 📅 미니 캘린더 | 오늘 날짜 하이라이트 캘린더 |

---

## 🚀 배포 방법

### 사전 준비
- Ubuntu 서버
- Nginx 또는 Apache2

### Nginx 설치 및 배포

```bash
# Nginx 설치
sudo apt update
sudo apt install nginx -y

# 서비스 시작
sudo systemctl start nginx
sudo systemctl enable nginx

# 파일 배포
sudo cp index.html /var/www/html/index.html
sudo chown www-data:www-data /var/www/html/index.html
```

브라우저에서 `http://서버IP` 로 접속하면 완료입니다.

---

## 📁 프로젝트 구조

```
nova-portal/
└── index.html   # 전체 소스 (HTML + CSS + JS 단일 파일)
```

---

## ⚙️ 커스터마이징

### 위치 변경 (날씨)
`index.html` 에서 아래 좌표를 원하는 도시로 교체하세요.

```js
// 현재: 분당
latitude=37.3595&longitude=127.1052

// 서울
latitude=37.5665&longitude=126.9780

// 부산
latitude=35.1796&longitude=129.0756
```

### 빠른 링크 추가
```html
<a href="https://example.com" target="_blank" class="qlink">
  <div class="qlink-icon" style="background:rgba(79,156,249,0.1)">🔗</div>
  <span>사이트명</span>
</a>
```

---

## 🛠 사용 기술

- **HTML / CSS / JavaScript** — 바닐라 단일 파일
- **[Open-Meteo API](https://open-meteo.com/)** — 무료 날씨 API (API 키 불필요)
- **[Google Fonts](https://fonts.google.com/)** — Syne, Noto Sans KR
- **Nginx** — 웹 서버

---

## 📄 라이선스

MIT License — 자유롭게 사용, 수정, 배포 가능합니다.
