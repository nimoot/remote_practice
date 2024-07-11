# VScode를 위한 명령어

```bash
# VScode로 '현재 작업 위치'에서 해당하는 'file_path'를 실행.
# 파일 위치 주소(file_path)
$ code {file_path}
```
# directory create
```bash
$ mkdir dir_name
```

# 현재 위치의 list
```bash
$ ls
```

# 파일 생성
```bash
$ touch {file_path}
```

# 파일 이동 및 수정
```bash
$ mv old_path new_path
# $ mv test_3.md test/
# 폴더명 수정 $ mv test new_test/
# 파일명 수정 $ mv intro.md 01_intro.md
```

# 삭제
```bash
# dir(디렉토리) 삭제와 파일 삭제는 다르다.

# 파일 삭제
$ rm {file_path}

# rm는 단일 객체 명령어만 삭제 가능


# dir 삭제
$ rm -r {dir_path}
# -r : recursion
```

# 작업 위치 옮기기
```bash
$ cd {dir_path}

# 현재 위치의 상위 경로로 작업 위치 옮기기
$ cd ..

```

## 절대 경로 VS 상대 경로
VScode에서는 전부 '상대 경로' 작성
- 상대경로
  - 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치를 작성한 것
  
# Git ('분산' 버전 관리 시스템)

- 중앙 집중식
  - 버전은 중앙 서버에 저장되고 중앙 서버에서 파일을 가져와 다시 중앙에 업로드
  - ex) mm에 내가 파일을 받고, 내가 수정했을 때 그 파일을 다시 넘겨줘야함
- 분산식
  - 버전을 여러 개의 복제된 저장소에 저장 및 관리
  - 버전의 수정/변경 사항만 저장
  
  Git의 역할
    - 코드의 버전(히스토리)을 관리
    - ### 개발되어 온 과정 파악
    - 이전 버전과의 변경 사항 비교

---

### Git의 영역
- Working Directory
  - PC에서 작업하고 있는 위치
  - GIT으로 관리가 되고 있을 수도 있고, 않을 수도 있다.
- Staging Area
  - add라는 명령어를 통해 다음 버전에 포함시켜야 될 파일을 모아놓는 곳
  - ex) commit이라는 명령어를 통해 새로운 버전을 생성
- Repository
  - 새로운 버전을 생성한 게 repo에 저장
  
- ### [WD] - add - [SA] - commit - [Repository]
  ---
  
```bash
$ ls -a
- .git/
  - 앞에 .이 붙으면 숨김 기능

$ git commit -m
- 커밋 메세지

$ git log
```
---
### Remote Repository (원격 저장소)
- 코드와 버전 관리 이력을 온라이 상의 특정 위치에 저장하여 여러 개발자가 협업하고 코드를 공유할 수 있는 저장 공간

