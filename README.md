## DA34-final-Football_Agora_chatbot_api 
- 서버상에 챗봇을 실행하고 응답을 주고받기 위한 API입니다.
- Fast API를 이용하여 구성하였습니다.


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






