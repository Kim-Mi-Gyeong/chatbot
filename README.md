# chatbot

gitbyb에 push하기 위한 과정
1) add: 바뀐내용 스테이징
git add chat.py
git add . (모든파일 스테이징)
2) commit: 그제서야 기록
git commit -m "테스트"
3) push: 리모트에 커밋된거 표시

1. 문제해결
   1) https://jjunii486.tistory.com/153
      (venv) D:\chatbot>git remote -v
      origin  origin (fetch)
      origin  origin (push)

      (venv) D:\chatbot>git remote remove june
      error: No such remote: 'june'

      (venv) D:\chatbot>git remote remove origin

      (venv) D:\chatbot>git remote add origin https://github.com/Kim-Mi-Gyeong/chatbot

      (venv) D:\chatbot>git remote -v            
      origin  https://github.com/Kim-Mi-Gyeong/chatbot (fetch)
      origin  https://github.com/Kim-Mi-Gyeong/chatbot (push)
