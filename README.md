# test-1
깃헙 연습하기

## 1. github의 핵심 구성
- branches: commit하는 주체. 필요에 따라 생성/소멸 시킨다.
- file-tracking: 버전관리대상 파일들은 생성/수정 과정을 거치면서 계속 변하고, 전후 비교할 경우가 많다. 그래서 이런 비교/수정을 기록하고
최종 확정되어 commit하게 될 파일들을 선정해 두는(stage에 올려놓는) 과정이 필요하다.  
  - git 행위 주체인 branches 정보가 표현되는 HEAD,
  - 행위 대상인 파일 정보로서 staged/unstaged 등으로 관리한다. 

![git_file-lifecycle](https://git-scm.com/book/en/v2/images/lifecycle.png)
- commit: 파일이 일단락 종결되었음을 선언한다.
- merge: 여러 갈래의 branches에서 commit 된 파일들을 종합한다.
- hub: github 등의 remote 중계 repository로 백업 및 협업을 한다.

### 1-1. 자주 사용하는 명령.
- git --help
```
$ git --help
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects

```
- git 행위 주체(branches) 관련
  - `git branch`: 모든 브랜치 목록을 보여주고, 현재 브랜치 이름 앞에는 `*`.
    - `git branch -d`/`-D`: 브랜치 삭제 / 병합안되어도 강제 삭제
  - `git switch <branchname>`: <branchname>으로 브랜치 변경
   

- `git init`: 현재 디렉토리 혹은 특정 디렉토리에서 git 시작.
- `git status`
- `git log`
- `git fetch`: remote repo를 불러온다.
- 'git diff`
## 2. 행위 pipeline에 따른 git 명령
### 2-1. 프로젝트의 시작
- team 여러 명이 brand-new 프로젝트를 시작할 때
  - 소 프로젝트를 각 자 진행하는 경우
  - 프로젝트를 중심으로 협업하는 경우
### 2-2. 프로젝트의 진행
- 프로젝트 진행 중에 신규 참여할 때
- 새로운 기능을 추가할 때
- 기존 버전을 수정해야 할 때
### 2-3. 프로젝트의 종결
- 최종 merge하고 종결.
