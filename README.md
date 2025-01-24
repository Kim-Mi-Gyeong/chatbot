# chatbot

gitbyb에 push하기 위한 과정
1) add: 바뀐내용 스테이징
git add chat.py
git add . (모든파일 스테이징)
2) commit: 그제서야 기록
git commit -m "테스트"
3) push: 리모트에 커밋된거 표시
git pus origin main

1. 문제해결
   1) 에러메세지 : Git: fatal: 'origin' does not appear to be a git repository --> https://jjunii486.tistory.com/153
      
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

    2) 에러메세지 : can't push refs to remote. try running 'pull' first to integrate your changes
      1차 확인
      (venv) D:\chatbot>git push origin branchname
      error: src refspec branchname does not match any
      error: failed to push some refs to 'https://github.com/Kim-Mi-Gyeong/chatbot'

      2차 확인
      (venv) D:\chatbot>git pull origin main --rebase
      remote: Enumerating objects: 9, done.
      remote: Counting objects: 100% (9/9), done.
      remote: Compressing objects: 100% (5/5), done.
      remote: Total 9 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
      Unpacking objects: 100% (9/9), 2.92 KiB | 19.00 KiB/s, done.
      From https://github.com/Kim-Mi-Gyeong/chatbot
       * branch            main       -> FETCH_HEAD
       * [new branch]      main       -> origin/main
      Successfully rebased and updated refs/heads/main.

      3차 확인 : 파일중에 API키 있는거 확인되어 삭제 후 push.

   

    
