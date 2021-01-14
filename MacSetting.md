# 맥 세팅하기

## 세팅 순서

1. [개발자 세팅](https://subicura.com/2017/11/22/mac-os-development-environment-setup.html)

2. [homebrew m1 세팅](https://subicura.com/2017/11/22/mac-os-development-environment-setup.html)
- brew 경로: /opt/homebrew
*/opt/homebrew로 경로 설정핮 않으면 'zsh: command not found: brew'에러 남*
```
cd /opt
mkdir homebrew && curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew
PATH=$PATH:/opt/homebrew/bin
sudo chown -R hachu /opt/homebrew
brew
```

3. [소스트리 다운로드](https://0urtrees.tistory.com/166)

4. node, npm, yarn homebrew로 설치 [Mac 에서 Homebrew 를 통해 node, npm, yarn 설치하기](https://butter-ring.tistory.com/17)
- 순서
  1. command+space bar
  2. terminall.app 실행
  3. 경ㄹ 이동 cd /opt
- 다운 예시: brew install node
- brew update: brew upgrade node brew upgrade yarn

5. ₩ 입력을 `로 바꾸기
- 옵션 + ₩ 눌러서 사용하도록 하자
- 다른 방법으로는 아래 방법이 있다
```
mkdir ~/Library/KeyBindings
touch DefaultkeyBinding.dict
echo “{ \”₩\” = (\”insertText:\”, \”\`\”); }” >> ~/Library/KeyBindings/DefaultkeyBinding.dict
```
### 문제 해결

*주의점*
- M1과 기존 인텔 일반 맥북고 세팅이 다를 수 있으니 M1용을 한번 더 검색해보기!

1. source tree push할 때 권한 문제로 안되는 경우
- 출처 : [push 권한 문제](https://blog.naver.com/xyz37/220056104469)
- 방법 
  - git remote remove origin
  - git remote add origin https://hachuu@github.com/hachuu/angular_page.git