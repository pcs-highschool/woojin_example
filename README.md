# 환경설정

1. node JS 설치
    1. [https://nodejs.org/ko/download/](https://nodejs.org/ko/download/)
2. git 설치
    
    windows
    
    - [https://git-scm.com/](https://git-scm.com/)
    - githubDesktop 설치해서 글로벌 계정 등록
    
    OSX
    
    - Xcode 설치 권장
3. VSCode 설치
    - [https://code.visualstudio.com/](https://code.visualstudio.com/)
    - extension pack 설치
    - <Vue VS Code Extension Pack>
4. Bash Terminal Open
    1. vscode → Ctrl + Shift + ` → new bash terminal

```shell
# yarn manager 설치
npm install -g yarn
```

6. 터미널에서 버전 확인
```shell
node -v
npm -v
yarn --version
```
7. vue-cli 설치
```shell
npm install -g @vue/cli
```
또는
```shell
yarn global add @vue/cli
```
8. vue project 생성
```shell
vue create {projectName}
```
    - 프로젝트 이름은 영문자 소문자와 - 만사용가능
    - Vue3 Default 선택
    - yarn 선택
```shell
cd {projectName}
yarn serve
```

### git repo 연동

1. 프로젝트 폴더 안까지 들어가야한다.
2. ls 해서 src 와 node_modules 폴더가 있는거 확인하고
```shell
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin [https://github.com/pcs-highschool/](https://github.com/pcs-highschool/){reposity name}
git push -u origin main
```