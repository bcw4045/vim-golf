# vim-golf
## 1. Add to quotes to ansible playbook

**문제**

해당 문제는 마지막 줄에 ""표를 넣는 문제이다.

최고점 : 8

나의 점수 : 8

**문제 파일**

![image](https://user-images.githubusercontent.com/67230834/144742168-5514ef1c-90d3-4a21-9bd4-d3828bde9766.png) ![image](https://user-images.githubusercontent.com/67230834/144742207-18d9b667-ea22-4f4c-957b-5e9e5c505241.png)

---

**풀이 과정**

```
GWi"<End><C-@>ZZ
```

![KakaoTalk_20211205_192022824](https://user-images.githubusercontent.com/67230834/144742697-ed282c13-e7b4-4e1d-ad80-7c1e9d25164d.gif)

**풀이 설명**

1번 문제의 경우 가장 아래에 변경할 문자열이 있으므로, G옵션으로 문서 맨 아래로 향한다.

이후 W옵션을 이용하여 다음 단어인 {앞으로 이동한다. 그 후 "문자를 삽인한 후 Ctrl+@ 옵션을 이용하여 이전에 삽인된 텍스트를 삽입하고 편집모드를 종료시킨다.

## 2. simple replacements

**문제**

해당 문제는 sublime과 emacs를 vim 문자열로 치환하는 문제이다.

최고점 : 19

나의 점수 : 27

**문제 파일**

![image](https://user-images.githubusercontent.com/67230834/144743334-77acc5f6-837f-4889-8849-5e577a79b1d7.png)  ![image](https://user-images.githubusercontent.com/67230834/144743342-4e871e9c-3ee0-462b-a524-f11d33da2d4e.png)

---

**풀이 과정**

```
W*cwvim<ESC>:%s/emacs/vim/g<CR><Esc>ZZ
```

![KakaoTalk_20211205_191906306](https://user-images.githubusercontent.com/67230834/144742723-773caa92-ad65-47f8-aedb-0f04cfc7e360.gif)

**풀이 설명**

2번 문제의 경우 가장 처음 행에 변경할 문자열이 있으므로, W옵션으로 해당 단어로 이동한다.

이후 \*옵션을 이용하여 해당 단어를 포워드 방향으로 찾는다. 이후 cw옵션을 이용하여 sublime을 vim으로 치환한다. 

다음으로 명령 모드로 진입하여 :%s/emacs/vim/g 명령을 이용하여 전체 문서에서 emacs를 vim으로 바꿔준다.

## 3. Satisfy the go linter

**문제**

해당 문제는 각 코드 위에 주석을 다는 문제입니다.

최고점 : 20

나의 점수 : 22

**문제 파일**

![image](https://user-images.githubusercontent.com/67230834/144742275-6ac02f8c-6b9b-4ea4-bf29-3e69f657799d.png)  ![image](https://user-images.githubusercontent.com/67230834/144742285-5bd11140-7d24-4b51-8677-90e6c6ee6084.png)

---

**풀이 과정**

```
4Gq1O// <C-N> TODO<Esc>q6G@1ZZ
```

![3_1](https://user-images.githubusercontent.com/67230834/144742764-4dfccb96-1c3c-4de7-b872-d2cc941ed532.gif)

![3_2](https://user-images.githubusercontent.com/67230834/144742777-8764a439-e12f-4bd4-aa7a-68494829d2c7.gif)

**풀이 설명**

3번 문제의 경우 같은 작업을 반복하므로 매크로를 이용하여 해결하였다. 가장 먼저 문자열을 삽입해야하므로 4G 옵션으로 해당 문자열로 이동한다.

이후 매크로 실행 옵션인 q를 실행시킨 후 매크로 이름을 1로 설정하였다. O옵션을 이용하여 바로 위에 문자열을 삽입할 수 있도록 커서를 이동시킴과 동시에 편집모드로 들어간다.

// 를 입력하고 <C-N> 옵션을 이용하여 Version을 자동 완성 시켜준다. 매크로 설정을 마치고 다음 문자열을 삽입해야할 장소로 6G 옵션을 이용하여 이동한다.
  
@1로 매크로를 실행시킨다.

## 4. Plotting some variables in python

**문제**

해당 문제는 함수 안의 문자열들을 맞는 문자열로 치환하는 문제입니다.

최고점 : 34

나의 점수 : 52

**문제 파일**
  
![image](https://user-images.githubusercontent.com/67230834/144743353-846caf99-9391-496f-a15e-c3b159cab1c9.png) ![image](https://user-images.githubusercontent.com/67230834/144743364-2ed78b8e-c2b1-4a84-abb8-ac890008826f.png)

---

**풀이 과정**

```
:%s/y1/abs(&)<CR>/k<KR>rgkrrkrb3G/1<CR>r2n.n.nr3n.n.nr4n.n.ZZ
```

![4_1](https://user-images.githubusercontent.com/67230834/144743524-3de5086a-943b-4b17-958b-810a0a0d0fd6.gif)

![4_2](https://user-images.githubusercontent.com/67230834/144743533-9a0ade09-730f-4206-96c0-f642eeb6b6d7.gif)

**풀이 설명**

4번 문제의 경우 처음으로 y1을 abs(y1)으로 바꿔주기 위해 :%s/y1/abs(&)옵션을 이용하여 문자열을 치환한다. 이후 /k로 k문자를 찾은 후 문자를 바꾸는 명령어인 r옵션을 이용하여 k를 치환시킨다.
  
나머지 숫자들을 치환시켜주기 위해 3G 옵션을 이용하여 3번째 줄로 이동한다. 이후 /1 옵션으로 1을 찾아준다. r 옵션을 이용하여 문자를 치환한 후 n으로 다음 1 문자로 이동한다. 
  
이후 바로 이전 명령을 반복하는 명령어인 .옵션으로 나머지 1 문자를 치환시켜준다.

## 5. Python dataclasses

**문제**

해당 문제는 맨 밑줄의 fields 변수의 ""안에 문자열을 집어넣는 문제이다.

최고점 : 19

나의 점수 : 19

**문제 파일**

![image](https://user-images.githubusercontent.com/67230834/144743636-c1407e10-7f37-4225-894b-00744299f0ac.png)  ![image](https://user-images.githubusercontent.com/67230834/144743645-fe920d2d-5e2e-40cb-a91e-6bae54348dce.png)

---

**풀이 과정**

```
G<BS>is<C-N><C-N>,n<C-N>,a<C-N>,sc<C-N><Esc>ZZ
```

![5번](https://user-images.githubusercontent.com/67230834/144743648-c172b757-d2e5-43c7-b612-81b0ceace09b.gif)

**풀이 설명**

5번 문제의 경우 마지막 행에 문자열을 삽입해야하므로 G 옵션으로 마지막 행으로 커서를 이동시킨다. 이후 백스페이스(<BS>)를 이용하여 문자열을 삽입해야하는 위치로 커서를 위치시킨다.
  
이후 자동완성 명령어인 <C-N> 옵션을 이용하여 각 문자들을 완성시켜준다.


