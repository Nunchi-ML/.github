<div align="center">

<img src="https://raw.githubusercontent.com/Nunchi-ML/.github/main/profile/assets/banner.png" width="100%" alt="눈치 Nunchi-ML"/>

<br/>

![기간](https://img.shields.io/badge/%EA%B8%B0%EA%B0%84-2026.10.29%20~%2011.10-555555?style=flat-square) ![iM Digital Banker Academy](https://img.shields.io/badge/iM%20Digital%20Banker%20Academy-%EB%A8%B8%EC%8B%A0%EB%9F%AC%EB%8B%9D%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-1E3A8A?style=flat-square) ![상태](https://img.shields.io/badge/%EC%83%81%ED%83%9C-%EC%99%84%EB%A3%8C-2E7D32?style=flat-square)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![scikit--learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white) ![LightGBM](https://img.shields.io/badge/LightGBM-2E7D32?style=flat-square) ![GeoPandas](https://img.shields.io/badge/GeoPandas-139C5A?style=flat-square) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![three.js](https://img.shields.io/badge/three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)

[![시뮬레이터](https://img.shields.io/badge/%EC%8B%9C%EB%AE%AC%EB%A0%88%EC%9D%B4%ED%84%B0-%EC%B2%B4%ED%97%98%ED%95%98%EA%B8%B0-FF8A20?style=flat-square)](https://nunchi-drive.vercel.app) [![발표 자료](https://img.shields.io/badge/%EB%B0%9C%ED%91%9C%20%EC%9E%90%EB%A3%8C-PDF-1E3A8A?style=flat-square)](https://github.com/Nunchi-ML/.github/releases/download/v1.0-final/nunchi_presentation.pdf) [![결과 보고서](https://img.shields.io/badge/%EA%B2%B0%EA%B3%BC%20%EB%B3%B4%EA%B3%A0%EC%84%9C-PDF-1E3A8A?style=flat-square)](https://github.com/Nunchi-ML/.github/releases/download/v1.0-final/nunchi_report.pdf) [![시연 영상](https://img.shields.io/badge/%EC%8B%9C%EC%97%B0%20%EC%98%81%EC%83%81-MP4-C92A2A?style=flat-square)](https://github.com/Nunchi-ML/.github/releases/download/v1.0-final/nunchi_demo.mp4) [![Notion](https://img.shields.io/badge/Notion-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%ED%99%88-000000?style=flat-square&logo=notion&logoColor=white)](https://app.notion.com/p/40554fa7e143815680c0cfb0ff414d78)

</div>

---

## 👀 눈치는

해가 정면에 낮게 들어오거나 밝은 도로에서 터널로 들어갈 때, 같은 길도 순간 앞이 잘 안 보입니다.<br/>
**눈치**는 이런 빛의 변화를 데이터로 먼저 알아채고, 그 구간에 들어가기 전에 미리 알려 주는 주행 안내입니다.

<img src="https://raw.githubusercontent.com/Nunchi-ML/.github/main/profile/assets/sim/sim_glare.jpg" width="100%" alt="눈치 드라이브 — 정면 눈부심 안내"/>

<p align="center"><sub>운전 시뮬레이터 「눈치 드라이브」 · 대구 달구벌대로 · 신천대로 · <a href="https://nunchi-drive.vercel.app">직접 체험하기 →</a></sub></p>

## 🧠 두 예측 모델

<table>
  <tr>
    <th width="50%">☀️ 태양광 눈부심 분류</th>
    <th width="50%">🚇 터널 암순응 분류</th>
  </tr>
  <tr>
    <td>사진 + 해 위치 · 날씨로<br/>정상 · 눈부심 · 심함을 판정</td>
    <td>터널 입구 사진으로<br/>안팎의 밝기 차이(하 · 중 · 상)를 판정</td>
  </tr>
  <tr>
    <td>두 단계 로지스틱 회귀<br/><b>평균 F1 0.640</b></td>
    <td>Ridge + 두 단계 로지스틱 회귀<br/><b>처음 보는 카메라 F1 0.844</b></td>
  </tr>
</table>

두 결과는 같은 사진인지 확인하는 통합 로직으로 묶어, 시뮬레이터에서 출발 전 · 주행 중 안내로 보여 줍니다.

## 🚗 눈치 드라이브

<table>
  <tr>
    <td width="50%"><img src="https://raw.githubusercontent.com/Nunchi-ML/.github/main/profile/assets/sim/sim_route.jpg" alt="출발 전 경로 판정"/><br/><sub>출발 전 · 코스 미리 판정</sub></td>
    <td width="50%"><img src="https://raw.githubusercontent.com/Nunchi-ML/.github/main/profile/assets/sim/sim_sign.jpg" alt="도로 전광판"/><br/><sub>도로 전광판 · 앞 구간 안내</sub></td>
  </tr>
  <tr>
    <td><img src="https://raw.githubusercontent.com/Nunchi-ML/.github/main/profile/assets/sim/sim_camera.jpg" alt="카메라 앱 판정"/><br/><sub>카메라 앱 · 바로 판정</sub></td>
    <td><img src="https://raw.githubusercontent.com/Nunchi-ML/.github/main/profile/assets/sim/sim_tunnel.jpg" alt="지하차도 밝기 변화"/><br/><sub>지하차도 · 밝기 변화 체험</sub></td>
  </tr>
</table>

## 🗂️ 저장소

| 저장소 | 내용 |
|---|---|
| 🧪 [Nunchi-ML_AI](https://github.com/Nunchi-ML/Nunchi-ML_AI) | 데이터 정제 · 실험 · 모델 학습과 추론 |
| ⚙️ [Nunchi-ML_BE](https://github.com/Nunchi-ML/Nunchi-ML_BE) | 눈부심 판정 API (FastAPI · Render) |
| 🎨 [Nunchi-ML_FE](https://github.com/Nunchi-ML/Nunchi-ML_FE) | 시뮬레이터 「눈치 드라이브」 (React · three.js) |

## 👥 팀 「눈치」

<table>
  <tr>
    <td align="center" width="150"><a href="https://github.com/FAITRUEE"><img src="https://github.com/FAITRUEE.png" width="96" alt="이성진"/><br/><sub><b>이성진</b></sub><br/><sub>팀장 · 눈부심 모델 · 시뮬레이터</sub></a></td>
    <td align="center" width="150"><a href="https://github.com/jaehyuck5"><img src="https://github.com/jaehyuck5.png" width="96" alt="최재혁"/><br/><sub><b>최재혁</b></sub><br/><sub>터널 암순응 모델</sub></a></td>
    <td align="center" width="150"><a href="https://github.com/kwonsuyoung0-rgb"><img src="https://github.com/kwonsuyoung0-rgb.png" width="96" alt="권수영"/><br/><sub><b>권수영</b></sub><br/><sub>기획 · 문서 · 보고서</sub></a></td>
    <td align="center" width="150"><a href="https://github.com/pbsu0413-byte"><img src="https://github.com/pbsu0413-byte.png" width="96" alt="박범수"/><br/><sub><b>박범수</b></sub><br/><sub>통합 주행 안내</sub></a></td>
  </tr>
</table>


<details>
<summary><b>📋 프로젝트 기록</b> — 일정 · 일하는 방식 · 프로젝트 지도</summary>

<br/>

| 단계 | 기간 | 끝나는 기준 | 상태 |
|---|---|---|:---:|
| 1️⃣ 주제 · 문제 정의 | 10/29 | 타깃과 사용 장면이 한 문장으로 | ✅ |
| 2️⃣ 기준 고정 | 10/30 | 평가 지표 · 분할 방식 · 기능 · API 입출력 확정 | ✅ |
| 3️⃣ 데이터 준비 · 분석 | 11/2 ~ 11/3 | 데이터 명세서 + 베이스라인 점수 | ✅ |
| 4️⃣ 모델링 | 11/4 ~ 11/6 | 모델별 대표 모델 · 추론 묶음 | ✅ |
| 5️⃣ 검토 · 마무리 | 11/9 ~ 11/10 | 보고서 · 발표 PPT · 시연 영상 (11/9 18:00 제출 · 11/10 발표) | ✅ |

```mermaid
flowchart LR
  A["📒 노션<br/>기준 문서"] --> B["📋 칸반<br/>데일리 스크럼"]
  B --> C["💬 슬랙<br/>[작업 시작]"]
  C --> D["🐙 이슈 · PR"]
  D --> E["📣 슬랙<br/>[작업 정리]"]
```

[🗺️ 프로젝트 지도](https://nunchi-ml.github.io/) · [👋 팀원 안내](https://app.notion.com/p/df8fb1d2f0db45dbab41cdd49edb5358) · [🐙 GitHub 컨벤션](https://app.notion.com/p/c86986ef9f3a4a3caedabfc16b6ff0b7) · [📦 최종 결과물 Release](https://github.com/Nunchi-ML/.github/releases/tag/v1.0-final)

</details>
