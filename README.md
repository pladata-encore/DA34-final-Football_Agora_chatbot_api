## DA34-final-Football_Agora_chatbot_api 

### About FutFut
<img src="https://github.com/ddsntc1/Chatbot_FutFut/assets/38596856/cb1cd8b7-c556-46a8-ab8d-e093af713433.jpg" width="400" height="400">


- 서버상에 챗봇을 실행하고 응답을 주고받기 위한 API입니다.
- Fast API를 이용하여 구성하였습니다.

---

#### 🚀 Use Tech
![Ubuntu](https://img.shields.io/badge/ubuntu-orange?style=for-the-badge&logo=ubuntu)
![HuggingFace](https://img.shields.io/badge/huggingface-yellow?style=for-the-badge&logo=HuggingFace)
![Colab](https://img.shields.io/badge/Colab-black?style=for-the-badge&logo=GoogleColab)
![Colab](https://img.shields.io/badge/FastAPI-cyanblue?style=for-the-badge&logo=FastAPI)

---

### To [Football_Agora](https://github.com/pladata-encore/DA34-final-Football_Agora)

---

### From [ddsntc1/ChatbotAPI](https://github.com/ddsntc1/FA_Chatbot_for_API)

---

### main.py 실행-> 서버에서 실행
```python
# 터미널 실행
uvicorn main:app --port <원하는 포트번호> --reload
```



### API 응답 호출 방법 -> django 내에서 모델 사용할 부분

```python
import requests
url = '주소:포트번호/query'
payload = {'query': 사용자가 입력한 query를 str형태로 입력받아융}
headers = {'Content-Type': 'application/json'}
response = requests.post(url, json=payload, headers=headers)
response.json() # 모델 응답 결과
# response.json()['response'][0].split('\\nAnswer')[-1][1:] 로 모델 응답부분 잘라주시면 감사하겠습니다
```


### Model repo

[풋풋이⚽](https://huggingface.co/Dongwookss/small_fut_final)






