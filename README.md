# vimgolf_OSS
vimgolf_OSS

### 1. Add quotes to ansible playbook
$ vimgolf put 5f0f5fbe280fbf000c233304

![1](https://user-images.githubusercontent.com/68629440/144738001-1deab3d0-2bc8-4d84-8ebf-40f839e9fe9a.gif)

`GWi"<End><C-@>ZZ`
* 점수: 8점
* 설명

`G`: 마지막줄 이동

`W`: 다음 단어 시작지점으로 이동

`i"`: 편집 모드 실행 후 `"` 작성

`<END>`: 라인의 끝으로 이동

`<C-@>`: 이전에 삽입한 텍스트(`"`)를 삽입하고 편집 종료

`ZZ`: 저장 후 종료

### 2. simple replacements
$ vimgolf put 603ba26a01b4d00009c10a49

![2](https://user-images.githubusercontent.com/68629440/144738724-9fbad438-7437-4e5b-bcc3-021ce6404ad2.gif)

`wcwvim<Esc>6j*qq.nq4@qZZ`
* 점수: 20점
* 설명

`w`: 다음 단어 시작지점 앞으로 이동

`cw`: 한 단어 삭제 후 수정

`vim<Esc>`: vim 입력 후 편집모드 나가기

`6j`: 6줄 아래로 이동

`*`: 커맨드 앞에 있는 단어와 같은 단어를 찾기

`qq`: @q를 입력하면 작동되는 q매크로 작성

`.`: 이전 명령어(`vim<Esc>`)를 다시 실행

`n`: 다음 탐색(`*` 커맨드로 찾은 단어들)

`q`: q매크로 작성 종료 (q매크로: `.n`)

`4@q`: q매크로를 4번 반복 실행

`ZZ`: 저장 후 종료

### 3. Satisfy the go linter
$ vimgolf put 5f1063aa8361810006e73210

![3](https://user-images.githubusercontent.com/68629440/144738738-34756f9f-d0bc-41de-8a67-dac024a5cd7d.gif)

`Gqq-O// <C-N> TODO<Esc>q@qZZ`
* 점수: 20점
* 설명

`G`: 마지막 줄로 이동

`qq`: q매크로 작성

`-`: 이전 줄로 이동

`O`: 행 위에 삽입, `// <C-N> TODO`를 입력 후 `<ESC>`로 편집모드 종료

`<C-N>`: 자동완성기능

`q`: q매크로 작성 종료 (q매크로: `-O// <C-N> TODO<Esc>`)

`@q`: q매크로 실행

`ZZ`: 저장 후 종료

### 4. Plotting some variables in python
$ vimgolf put 9v0060da5177000000000209

![4](https://user-images.githubusercontent.com/68629440/144739120-4e052d07-7a93-4d1b-b99e-ad267c996f70.gif)

`jfyiabs(<Right><Right>)<Esc>qqYjVp<C-A>w<C-A>fa<C-A>q2@qFkrgkrrkrbZZ`
* 점수: 40
* 설명

`j`: 아래로 이동

`f(y)`: 앞쯕으로 가장 먼저 발견되는 y로 이동

`i`: 편집 모드 실행

`abs(<Right><Right>)<Esc>`: 작성 후 편집 모드 종료

`qq`: q매크로 작성

`Y`: 줄 복사

`j`: 아래로 이동

`V`: 줄 비주얼 모드

`p`: 붙여넣기

`<C-A>`: 가장 먼저 만나는 숫자의 크기를 늘려줌

`w`: 다음 단어 시작지점 앞으로 이동

`f(a)`: 앞쯕으로 가장 먼저 발견되는 a로 이동

`q`: q매크로 종료 (q매크로: YjVp<C-A>w<C-A>fa<C-A>)

`2@q`: q매크로 2회 실행

`F(k)`: 뒤쪽으로 가장 먼저 발견되는 k로 이동

`r`: 한 글자만 교체
  
`k`: 위로 이동
  
`ZZ`: 저장 후 종료
