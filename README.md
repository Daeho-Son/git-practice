# 소개
- `git merge` 시, `Fast-forward Merge`와 `3-way Merge`를 확인하기 위한 자료 
- 학습 자료: [https://sondho.tistory.com/112](https://sondho.tistory.com/112)


# 실습에 사용되는 브랜치
- `dev/merge`
  - 병합(Merge) 실습을 위한 브랜치
- `feat/merge-ff`
  - `Fast-forward Merge`를 확인하기 위한 브랜치
  - `dev/merge` 브랜치에서 한 개의 브랜치가 추가로 커밋됐다.
- `feat/merge --no-ff`
  - `3-way Merge`를 확인하기 위한 브랜치
  - `dev/merge` 브랜치에서 한 개의 브랜치가 추가로 커밋됐다.
- `dev/merge\'1`
  - `3-way Merge`를 확인하기 위한 브랜치로 `dev/merge` 브랜치에서 한 개의 브랜치가 추가로 커밋됐다.


# 실습에 사용되는 `git merge`의 옵션
- `--ff`
  - `Fast-forward Merge`로 동작한다.
- `--no-ff`
  - `3-way Merge`로 동작한다.


# 참고
- 명령어 실행 후, 어떤 메시지가 출력되는지 확인하세요.
- 실습하면서 중간에 `ls`, `git log`, `git log --graph` 등 명령어를 통해 변경되는 걸 확인하세요.
- 한 개 실습 후, `git reset --hard HEAD^`를 통해 실습 전으로 되돌리면 다음 실습이 편합니다.


# 실습

## [dev/merge](https://github.com/Daeho-Son/git-practice/commits/dev/merge/)
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


## [dev/merge'1](https://github.com/Daeho-Son/git-practice/commits/dev/merge'1/)
  ```bash
  $ git checkout dev/merge\'1
  $ git merge feat/merge-ff
  $ git log --graph
  ```

## [feat/merge-ff](https://github.com/Daeho-Son/git-practice/commits/feat/merge-ff/)
| `dev/merge` 에서 생성된 브랜치. 부모 브랜치보다 커밋 한 개 추가됨

| `merge-ff-feat` 라는 파일 추가 후, 원격 저장소로 업로드된 상태


<br>
