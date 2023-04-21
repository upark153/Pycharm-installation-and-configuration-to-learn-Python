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
