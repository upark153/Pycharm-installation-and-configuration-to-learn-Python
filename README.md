# Pycharm-installation-and-configuration-to-learn-Python\
![image](https://user-images.githubusercontent.com/115389450/233526226-a948e3ee-27b7-41fb-83ae-3c275deb8b6e.png)

- - -
제비뽑기
- - -
```
import random
import tkinter
def click_btn(): // 버튼 문자열 변경 함수 > 라벨 문자열 무작위로 변경
    label["text"] = random.choices(["강민영", "고연재", "김기태", "김명은", "김성일", "김연수", "김재일", "노도현", "류가미", "박규환", "박성빈", "박시형", "박의용", "오송화", "이범규", "이보라", "이소윤", "이여름", "이지혜", "이현도", "임성경", "임영효", "임홍선", "장은희", "정연우", "정철우", "주민석", "최지혁"])
    label.update()

root = tkinter.Tk() // 윈도우 요소(객체) 생성
root.title("뽑기 프로그램") // 윈도우 제목 지정
root.resizable(False,False) // 명령으로 윈도우 크기를 변경하지 못하게 한다.
canvas = tkinter.Canvas(root, width=800, height=600)
canvas.pack()
gazou = tkinter.PhotoImage(file="귀멸의칼날.png")
canvas.create_image(400,300,image=gazou)

label = tkinter.Label(root,text="??", font=("Times New Roman",60), bg="white") /
label.place(x=480,y=60) 

button = tkinter.Button(root,text="청소당번뽑기", font=("Times New Roman", 36), fg="skyblue", command=click_btn) // 버튼생성, command 인자로 클릭시 호출할 함수 지정
button.place(x=460,y=400)
root.mainloop() // 화면에 윈도우 표시
```
[참조한사이트](https://jinho-study.tistory.com/1077)


<video src='https://user-images.githubusercontent.com/115389450/233526876-9be1b720-d612-4f45-848d-daf4873e1798.mp4' width=180/></video>
![image](https://user-images.githubusercontent.com/115389450/233527009-4620405b-0bb0-4476-b222-90af0684279a.png)

![image](https://user-images.githubusercontent.com/115389450/233527312-17b2c9c9-c869-4ea2-837e-a41740f3f29d.png)
```
studentScore = [] // 이름, 점수를 관리 해줄 리스트

while True:  // while에 True를 지정하면 무한 루프
       choice = int(input('[1]시험점수입력 [2]성적확인 [3]종료 ')) // 1, 2, 3 중 하나를 선택

       if choice ==3: // 3을 선택하면
              break // 반복문 탈출
       elif choice == 1: //1을 선택하면
              name = input('이름 입력 : ')  // name이라는 변수에 입력한 이름 저장
              kor = int(input('국어 점수 입력 : ')) // kor이라는 변수에 국어 점수 저장
              eng = int(input('영어 점수 입력 : ')) // eng이라는 변수에 영어 점수 저장
              mat = int(input('수학 점수 입력 : ')) // mat이라는 변수에 수학 점수 저장
              clang = int(input('C언어 점수 입력 : ')) // clang 이라는 변수에 c언어 점수 저장

              studentScore.append([name, kor, eng, mat, clang]) // append 하나의 값만 추가 가능, 이름,점수 모두 보관해야 하므로 하나의 값으로 > 리스트로 묶어서
       elif choice ==2:
              print(' '*15,'성','   ','적','   ','표')
              print('-'*50)
              print('이름    ', '국어    ', '영어   ', '수학   ',  'C언어   ','평균   ')

              for s in studentScore:
                     avg = (s[1]+s[2]+s[3]+s[4])/4 // 사람마다 점수가 다르니 반복문으로 하나씩
                     print(f'{s[0]}\t{s[1]}\t\t{s[2]}\t\t{s[3]}\t\t{s[4]}','  ' ,avg) // \t는 탭간격, f'[s숫자]는 위에서 입력한 순서대로 이름>국어>영어>수학>c언어
```
![image](https://user-images.githubusercontent.com/115389450/233527390-ec7eb066-0388-4a59-acc2-51c4d9aac918.png)

![image](https://user-images.githubusercontent.com/115389450/233527444-e90e6876-a37f-4d4d-acf7-ca07df0664ee.png)
```
Instring = input('입력 : ')
Dic = {}
idx = 0
for ch in Instring:
    if ch not in Dic:
        Dic[ch] = []
        Dic[ch].append(idx)
        idx +=1
for ch in Dic:
    print(f'{ch}:count')
    len(Dic[ch])
    print(Dic[ch])
```
![image](https://user-images.githubusercontent.com/115389450/233527488-b5386f05-1c9f-4cda-8b17-6d4c5d4b0a8b.png)
```
Instring = input('입력 : ')
Dic = {}
idx = 0
for ch in Instring:
    if ch not in Dic:
        Dic[ch] = []
    Dic[ch].append(idx)
    idx +=1
for ch in Dic:
    print(f'{ch}:count는{len(Dic[ch])}, index는 {Dic[ch]}')
```
![image](https://user-images.githubusercontent.com/115389450/233527533-2177b206-ff32-45ec-9c68-3aecf1299c1f.png)

![image](https://user-images.githubusercontent.com/115389450/233527653-221089d7-314b-43dc-a922-40708436714e.png)

[파이썬공식문서참조](https://docs.python.org/3/library/stdtypes.html#range)
![image](https://user-images.githubusercontent.com/115389450/233527809-68916e3b-085b-4101-9a89-0f50a43aa15c.png)
```
a = 'o'
print("*")
print("o*")
print("oo*")
print("ooo*")
print("oooo*")
for i in range(0, 5):
    print(f'{i*a}*')
```
![image](https://user-images.githubusercontent.com/115389450/233527896-a1baf755-c5b7-45a1-933d-c5c1051506b5.png)
```
a = '*'
print("*****")
print("****")
print("***")
print("**")
print("*")
for i in range(0, 5):
    print(f'{a*(5-i)}')
```
![image](https://user-images.githubusercontent.com/115389450/233527961-a695e336-bd59-4ec3-bf94-c474757d7605.png)
```
# 공백이 4,3,2,1,0로 줄어든다.
# 별이 1,3,5,7,9로 늘어난다.
# 홀수 표현하는 방법? i*2+1 // 여기서 i는 0,1,2,3,4로 증가하고 5가 되면 반복문 종료
# 그렇다면 반복문은 2개를 사용해야 하는 것일까?
print("    *")
print("   ***")
print("  *****")
print(" *******")
print("*********")

blank = ' '
star = "*"

for i in range(0, 5):
    print(f'{blank*(4-i)}'f'{star*(i*2+1)}', end="") 
    print() // 요 녀석은 출력을 담당
```
![image](https://user-images.githubusercontent.com/115389450/233528030-89262c0a-82e7-48f9-a570-9d0aa0b5e0b1.png)
```
print("    *")
print("   ***")
print("  *****")
print(" *******")
print("*********")

blank = ' '
star = "*"

for i in range(0, 5):
    print(f'{blank*i}'f'{star*(10-(i*2+1))}', end="")
    print()
```
![image](https://user-images.githubusercontent.com/115389450/233528100-95e513ca-5cd9-4fdf-8831-fb57377452be.png)
```
blank = ' '
star = "*"

for i in range(0, 5):
    print(f'{blank*(4-i)}'f'{star*(i*2+1)}', end="")
    print()
for i in range(0, 5):
    print(f'{blank*i}'f'{star*(10-(i*2+1))}', end="")
    print()
```
![image](https://user-images.githubusercontent.com/115389450/233528150-49ee37dc-8303-4b7f-a4fb-fba331b5d101.png)
```
blank = ' '
star = "*"

for i in range(0, 7):
    print(f'{blank*(i+1)}'f'{star*(14-(i*2+1))}', end="")
    print()
for i in range(0, 7):
    print(f'{blank*(7-i)}'f'{star*(i*2+1)}', end="")
    print()
```
![image](https://user-images.githubusercontent.com/115389450/233528194-c4fc795a-3928-4915-bc2c-685f3910d553.png)
- - -
바람개비를 다시 그려보시오 
- - -
```
a = '*'
b = ' '

for i in range(0, 10):
    print(f'{a*(i+1)}'f'{b*(10-i)}'f'{a*(10-i)}', end=" ")
    print()
for j in range(0,10):
    print(f'{b*(10-j)}'f'{a*(j+1)}'f'{b*(j+1)}'f'{a*(10-j)}', end= " ")
    print()
```
![image](https://user-images.githubusercontent.com/115389450/233528254-6d3e6157-1f5b-4b66-822c-83724a511174.png)
```
a = '*'
b = ' '
c = int(input())

for i in range(0, c):
    print(f'{a*(i+1)}'f'{b*(c-i)}'f'{a*(c-i)}', end=" ")
    print()
for j in range(0, c):
    print(f'{b*(c-j)}'f'{a*(j+1)}'f'{b*(j+1)}'f'{a*(c-j)}', end= " ")
    print()
```
![image](https://user-images.githubusercontent.com/115389450/233528304-d166f002-22f9-461e-9411-b8f6d0885f46.png)








