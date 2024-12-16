---
description: How to commit git
---

# Git basic

* ## Repository

```python
git init #make current repository .git폴더 생성(hidden folder)
```

* ## Commit

현재 변경  사항을 특정 버전으로 남기는 것

1. Working directory

* 내가 실제로 작업하고 있는 디렉토리

2. Staging Area

* commit으로 남기고 싶은, 특정 버전으로 관리하고 싶은 파일이 모여있는 곳

3. Repository

* commit들이 저장되는 곳

***

* ## Command

```python
git add {file name} # add to Staging Area
        # add하지 않은 file은 untracked  상태
        # add한 file은 tracked 상태
git add {file name1} {file name2} # 여러개의 파일 add
git add . #현재 folder내의 모든 file들을 Staging Area로 add
```

```python
git commit     
gir commit -m "commit message" # Staging Area to Repository(committed)
```

```python
git status # view working directory and staging area status
```

```python
git config --global user.name "user name" 
git config --global user.email "user email" 
# adding acount information to Git
```

```python
git log #view the commit history of a Git repository
git log --oneline # view simple log
git log -n <number> # 가장 최근의 N개 커밋만 표시
git log <file name> # 특정 파일에 대한 변경 이력만 확인
git log --graph # 시각적으로 보여줌
```

{% hint style="info" %}
commit된 파일을 수정 후 git status로 확인 시 modified 파일로 뜸
{% endhint %}

***

## Local Repository → Remote Repository

commit기반으로 연결

* Github에서 create New repository

```bash
git remote add origin {New repository https}
# https주소를 origin에 할당(관례)

git branch -M main(master)
# master 를 main으로 변경

git push -u origin main(master) 
# u = upstream
```



## Remote Repository → Local Repository&#x20;

Clone

* Github에서 Repository 선택

```bash
git clone {repository https}

Local Repository에서 파일생성 후 git add → git commit까지 시켰다면
git push로 바로 업데이트

open . # current folder open 
start . # current folder open
```




















