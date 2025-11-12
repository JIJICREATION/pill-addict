# 📘 프로젝트 개요

Pill Addict는 사용자의 건강검진표를 OCR로 인식해 주요 수치를 자동 추출하고,  
이를 기반으로 GPT API가 개인 맞춤형 영양제 및 생활습관 조언을 제공하는 AI 챗봇 서비스입니다.  

FastAPI로 구현된 백엔드를 AWS EC2 환경에 배포하고,  
Streamlit 기반 UI를 통해 사용자가 웹 환경에서 실시간으로 대화하고 결과를 확인할 수 있도록 개발하였습니다.  

---

# 🧱 기술 스택

| 구분 | 사용 기술 |
|------|-------------|
| **Backend** | FastAPI, Python, Uvicorn |
| **Frontend** | Streamlit |
| **AI / LLM** | OpenAI GPT API, Prompt Engineering |
| **OCR** | Tesseract OCR |
| **Vector DB** | FAISS, Weaviate (설계 및 제안 반영) |
| **Infra** | AWS EC2 (Ubuntu) |

---

# 👥 역할

| 이름 | 역할 | 주요 담당 |
|------|------|------------|
| **지민성 (본인)** | 프로젝트 매니저 / UI 및 배포 담당 | 프로젝트 기획 및 일정 관리<br>GPT API 연동 및 Prompt Engineering<br>FastAPI 서버 구축 및 AWS EC2 배포<br>Streamlit UI 디자인 및 구현<br>통합 테스트 및 성능 검증<br>FAISS / Weaviate 벡터DB 구조 제안 |

---

# ⚙️ 주요 기능

- 건강검진표 이미지를 업로드하면 Tesseract OCR을 이용해 주요 텍스트 자동 추출  
- 추출된 데이터를 GPT API에 전달하여 영양제 및 생활습관 조언 생성  
- Streamlit UI에서 업로드 및 대화형 챗봇 기능 제공  
- FastAPI 서버 – Streamlit UI 간 실시간 통신 구조 설계  
- AWS EC2 환경에 FastAPI 서버를 Uvicorn으로 직접 배포 및 운영  

---

# 📂 프로젝트 구조

pill-addict/
├── app/
│ ├── main.py # FastAPI 서버 (AWS EC2 배포)
│ ├── ocr_utils.py # Tesseract OCR 처리 모듈
│ └── recommender.py # GPT 기반 추천 및 응답 생성
├── frontend/
│ └── streamlit_app.py # Streamlit UI
├── data/
│ └── sample_health_check.png
├── requirements.txt
└── README.md
