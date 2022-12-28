# 12월 28일 복습

## 버전 관리


- 저장소 처음 만들 때 : $ git init

- 버전 기록 

```
    $ git add <file>
    $ git commit -m '<커밋메시지>'
```

- 상태 확인

```
    $ git status : 1통, 2통
    $ git log : 커밋 확인
```

---

## 원격저장소 명령어

```
    $ git clone <url> : 원격저장소 복제

    $ git remote -v : 원격저장소 정보 확인

    $ git remote add <원격저장소> <url> : 원격저장소 추가  
     * 원격저장소는 국제적 표준인 origin으로 통일, 브랜치는 master or main 

    $ git remote rm <원격저장소> : 원격저장소 삭제

    $ git push <원격저장소> <브랜치> : 원격저장소에 Push
     * Push : 로컬저장소 버전을 원격저장소로 보낸다.

    $ git pull <원격저장소> <브랜치> : 원격저장소에 Pull           
     * Pull : 원격저장소의 버전을 로컬저장소로 가져온다.
```

#### - Push 오류

1) 원격저장소의 커밋을 원격저장소로 가져온다.
    
    $ git pull origin master

2) 로컬에서 두 커밋을 병합한다.

    동시에 같은 파일이 수정된 경우 merge conflict가 발생할 수 있으므로 브랜치가 필요함. 

3) 다시 Github로 Push 작업을 한다.

    $ git push origin master

***

## .Gitignore


- 버전 관리를 별도로 하지 않는 파일/디렉토리 발생

- Git 저장소에 .gitignore 파일 생성 후 해당 내용 관리

- 작성 예시

    1) 특정 파일 : a.txt(모든 a.txt), test/a.txt(테스트 폴더의 a.txt)

    2) 특정 디렉토리 : /my_secret

    3) 특정 확장자 : *.exe

    4) 예외 처리 : !b.exe

- 이미 커밋된 파일은 반드시 삭제를 하여야 .gitignore로 적용됨
