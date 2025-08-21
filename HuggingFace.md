# 🤗 Hugging Face 쉬운 소개

---

## 🤔 Hugging Face란?

- 인공지능(AI) 모델을 **쉽게 사용하고 공유**할 수 있게 도와주는 플랫폼이에요.
- **웹사이트**, **라이브러리**, **API**로 구성되어 있어요.

> 마치 "깃허브 + 앱스토어 + 모델실행기"를 합쳐 놓은 느낌!

---

## 🌍 어떤 기능들이 있나요?

| 기능              | 설명                                                                 |
|-------------------|----------------------------------------------------------------------|
| 🧠 모델 저장소      | 전 세계 사람들이 만든 AI 모델을 검색하고 가져다 쓸 수 있어요.         |
| 🛠️ Inference API   | 모델을 서버 없이 바로 실행할 수 있어요. (초간단 실행 버튼!)            |
| 💬 Transformers    | 텍스트 관련 모델(번역, 요약, 감정분석 등)을 다룰 수 있는 파이썬 라이브러리 |
| 🔐 Spaces           | 직접 만든 AI 데모를 웹사이트처럼 배포할 수 있어요 (코딩 + 공유 완료!)   |

---

## 🔗 Hugging Face는 "웹사이트"예요?

네! 아래 주소로 접속하면 돼요:

👉 [https://huggingface.co](https://huggingface.co)

---

## 💡 대표적으로 이런 모델들이 있어요:

| 이름                          | 하는 일                 |
|-------------------------------|--------------------------|
| `bert-base-uncased`          | 문장 이해                |
| `facebook/bart-large-cnn`    | 긴 글 요약               |
| `nlptown/bert-base-multilingual` | 감정 분석 (다국어)     |
| `gpt2`                        | 글 자동 생성              |

---

## 🛠️ 사용법은?

### ✅ 1) 웹사이트에서 바로 써보기

- 모델 페이지에 가서 로그인하고 **"Compute"** 버튼 누르면 끝!
- 예: [https://huggingface.co/facebook/bart-large-cnn](https://huggingface.co/facebook/bart-large-cnn)


<img width="486" height="310" alt="image" src="https://github.com/user-attachments/assets/ca67ff4c-be6d-43a9-9c4f-4dbc21e81597" />

---

### ✅ 2) Python 코드로 사용 (Transformers 라이브러리)

```python
from transformers import pipeline

summarizer = pipeline("summarization")
result = summarizer("너무 긴 텍스트를 요약해주는 모델입니다...")
print(result[0]['summary_text'])
```

---

### ✅ 3) 서버 없이 Inference API 사용

```http
POST https://api-inference.huggingface.co/models/facebook/bart-large-cnn
Authorization: Bearer hf_your_token

Body:
{
  "inputs": "요약할 텍스트"
}
```

