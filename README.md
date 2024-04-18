# 소개
- Github 연습용 레포

<br>

# 실습 브랜치
## --ff, --no-ff  [(공부 자료)](https://sondho.tistory.com/112)
### 참고
- 명령어 실행 후, 어떤 메시지가 출력되는지 확인하세요.
- 실습하면서 중간에 `ls`, `git log`, `git log --graph` 등 명령어를 통해 변경되는 걸 확인하세요.
- 한 개 실습 후, `git reset --hard HEAD^`를 통해 실습 전으로 되돌리면 다음 실습이 편합니다.

### [dev/merge](https://github.com/Daeho-Son/git-practice/commits/dev/merge/)
| 브랜치 병합 실습을 하기 위한 브랜치

`git merge` 명령어를 통해 `Fast-forward Merge` 확인
  ```bash
  $ git checkout dev/merge
  $ git merge feat/merge-ff
  $ git log --graph
  ```

`git merge --no-ff` 명령어를 통해 `3-way Merge` 확인
  ```bash
  $ git checkout dev/merge
  $ git merge --no-ff feat/merge-ff
  $ git log --graph
  ```


### [dev/merge'1](https://github.com/Daeho-Son/git-practice/commits/dev/merge'1/)
| `dev/merge` 에서 생성된 브랜치로 부모 브랜치보다 커밋 한 개 추가됨

`git merge` 명령어를 통해 `3-way Merge` 확인
  ```bash
  $ git checkout dev/merge\'1
  $ git merge feat/merge-ff
  $ git log --graph
  ```

### [feat/merge-ff](https://github.com/Daeho-Son/git-practice/commits/feat/merge-ff/)
| `dev/merge` 에서 생성된 브랜치로 부모 브랜치보다 커밋 한 개 추가됨
| `merge-ff-feat` 라는 파일 추가 후, 원격 저장소로 업로드된 상태


<br>
