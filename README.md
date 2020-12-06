# 주피터노트북

jupyter-notebook --no-browser --port=8080 python_work (로컬)
jupyter-notebook --no-browser --port=8080 --ip=* python_work (공용)

-----------------------------------------------------------------
# for & while

## range(a,b)
> a ~ b 범위 숫자를 발생
```
range(5) = (0,5)
r = range (5) = (0,5)

for x in range(5):
    print(x)
```
결과 : 0 1 2 3 4 
```
for x in r : 
    print(x)

for x in range(10, 100, 4):
    print( x * '*')
```
결과 : 최소값 10부터 최대값 100까지 4개씩 * 이 증가하며 출력된다
```
for x in range(1,20):
    if x % 2 == 0: #짝수
        print (x * '*')
    else : 
        print (x * '+')
```
결과값 = 최소값 1부터 최대값 20까지 짝수(2로나눈 나머지가 0인수)는 * 이 출력되고
나머지(홀수)는 + 가 출력된다.

-----------------------------------------------------------------
```
x = 0
while x < 5 :
    print('A')
    x += 1
```
결과값 = x가 0부터 4(5 미만)까지 1씩 더해지며 A를 출력한다 (총 A 다섯번 출력)

-----------------------------------------------------------------

x = 0
while x true :
    print('A')
    x += 1
    if x == 300: #종료조건
	break

결과값 = 총 300번 A를 출력하고 멈춘다(break)

-----------------------------------------------------------------

while True :
    stop = int(input('끝 숫자를 입력:'))
    if stop == -1:
        print('Quit....'); break
        
    sum = 0
    for i in range(1,stop) :
        if i%3 == 0 :
            print('%d' % i, end = ' ')
            sum += i
        
    print('\n','_' * 50)
    print(f'1~{stop} 에서 3의 배수 합계 : {sum}')

 결과값 = 끝 숫자를 입력:30
3 6 9 12 15 18 21 24 27 
__________________________________________________
1~30 에서 3의 배수 합계 : 135
끝 숫자를 입력:-1
Quit....

 --------------------------------------------------

n1 = int(input('시작 수를 입력하세요 : '))
n2 = int(input('끝 수를 입력하세요 : '))

sum = 0
for i in range(n1,n2+1) : #n1부터 n2미만까지만 구하기때문에 +1
    if i%5 != 0 : #5의 배수가 아닌 수를 구해야하기때문에 !=
        sum += i 
        
print('_' * 50)
print('%d에서 %d까지 5의 배수가 아닌 수의 합 %d' % (n1,n2,sum))

결과값 = 

시작 수를 입력하세요 : 100
끝 수를 입력하세요 : 200
__________________________________________________
100에서 200까지 5의 배수가 아닌 수의 합 12000

 --------------------------------------------------

phone = input('하이픈(-)을 뺀 11자리의 휴대폰 번호를 입력하세요 : ')

number = '';

for i in range(0 , len(phone)) :
    if i == 2 :
        number = number + (phone[2]+'-')
    elif i == 6 : 
        number = number + (phone[6] + '-')
    else : 
        number = number + phone[i]
        
print(number);

결과값 = 
하이픈(-)을 뺀 11자리의 휴대폰 번호를 입력하세요 : 01012345678
010-1234-5678

 --------------------------------------------------

for i in range(2,10) :
    for b in range (1,10) :
        a = i*b
        print("%d x %d = %d" % (i , b, a)) # %뒤에 인자가 여러개라면 꼭 괄호 붙이기

결과값 = 구구단

 --------------------------------------------------

#별찍기 

for i in range(1,11) :
    for j in range(1,i+1) :
        print('*',end="")
    print()

결과값 = 

*
**
***
****
*****
******
*******
********
*********
**********
 --------------------------------------------------
#입력받아서 별찍기

s = int(input("세로길이를 입력하세요 : "))
g = int(input("가로길이를 입력하세요 : "))

for x in range(0,s) :
    
    for j in range(0,g) : 
        
        print(" * ",end = "")
    
    print()

print()

결과값 =

세로길이를 입력하세요 : 5
가로길이를 입력하세요 : 10
 *  *  *  *  *  *  *  *  *  * 
 *  *  *  *  *  *  *  *  *  * 
 *  *  *  *  *  *  *  *  *  * 
 *  *  *  *  *  *  *  *  *  * 
 *  *  *  *  *  *  *  *  *  *

 --------------------------------------------------

#섭씨를 화씨로 바꾸기

print('-' * 30) #줄
print(' 섭씨 화씨')
print('-' * 30) #줄

c=-20 #섭씨
while c<41 : #섭씨가 40도가 될때까지
    f = c*9.0/5.0+32.0 #화씨
    print('%8d %8.1f' % (c,f))
    
    c+=1 #-20에서 1씩 증가 
    
print('-' * 30) #줄

*******************************************

#리스트

li = [1,2,3,4,5] #변수선언

 --------------------------------------------------

li
결과값 = [1, 2, 3, 4, 5]

 --------------------------------------------------

type(li[3])
결과값 = int

 --------------------------------------------------

li[3] = 10
print(li[3])
결과값 = 10

 --------------------------------------------------

list(range(1,10,3))
결과값 = [1, 4, 7]

 --------------------------------------------------
#리스트 더하기,곱하기 연산

a = list("안녕하세요")
b =  list('빨주노초파남보')

a+b = ['안', '녕', '하', '세', '요', '빨', '주', '노', '초', '파', '남', '보']

a*2 = ['안', '녕', '하', '세', '요', '안', '녕', '하', '세', '요']

 --------------------------------------------------
list() #리스트를 만든다

list("안녕하세요")
결과값 = ['안', '녕', '하', '세', '요']

.join() #리스트 중간중간에 ""안에 들어가는 문자를 넣는다

list_a = list("안녕하세요")
"*".join(list_a)

결과값 = '안*녕*하*세*요'

.append() #리스트 맨뒤에 괄호안에 넣은 것을 추가

list_a.append('뷃')

결과값 = ['안', '녕', '하', '세', '요', '뷃']

.insert #(인덱스,바꿀것) 

list_a.insert(1,'먐') #인덱스 1번째의 글자(녕)를 먐으로 변경

결과값 = ['안', '먐', '녕', '하', '세', '요']

.index() #괄호안에 적은 글자의 인덱스번호를 가져온다

list_a = list("가나다라마바사")

list_a.index("나")

결과값 = 1   #"나"의 인덱스번호

clear #list_a.clear = a의 리스트를 초기화

count #list_a.count("가") = 리스트 list_a에서 "가"의 개수가 몇개인지 탐색

sort # list_a.sort() = 리스트 list_a의 값을 순서대로 정렬 ex) 가나다 순

sorted #sorted(list_a) = 리스트 list_a의 값을 순서대로 정렬

remove #list_a.remove("가") = 리스트 list_a의 요소 중 "가" 를 삭제

.pop() #list_a.pop(2) = 리스트 list_a의 인덱스2번째의 요소를 지운후 반환 ,
list_a.pop() = 리스트 list_a의 제일 마지막 요소를 지운 후 반환

#del
list_c = ["a","b"]
g = 10

del list_c[0] #c리스트의 0번째 요소를 삭제
del g = g 전체를 삭제

--------------------------------------------------

mylist = ['사과','바나나','파인애플','배']
mylist.append('키위')

for a in mylist :
    print(a)

결과값 = 

사과
바나나
파인애플
배
키위

--------------------------------------------------

#for로 list에 있는 값 평균 구하기

scores = [88,75,90,95,77,69,80,92]

sum = 0
for score in scores : #scores에 있는 값을 하나씩 score로
    sum += score #총점
   
    avg = sum/8 #평균
    
    print('총점 : %d, 평균:%.2f' % (sum,avg))

결과값 =

총점 : 88, 평균:11.00
총점 : 163, 평균:20.38
총점 : 253, 평균:31.62
총점 : 348, 평균:43.50
총점 : 425, 평균:53.12
총점 : 494, 평균:61.75
총점 : 574, 평균:71.75
총점 : 666, 평균:83.25

--------------------------------------------------

#수우미양가 개수 구하기

s = [64,89,100,85,77,58,79,67,96,87,87,36,82,98,84,76,63,69,53,22]

count_su = 0 # 90~100점 (수)
count_woo = 0 # 80~89점 (우)
count_mi = 0 # 70 ~ 79(미)
count_yang = 0 # 60 ~ 69(양)
count_ga = 0 # 0 ~ 59(가)

i = 0

while i < len(s) :
    if s[i] >= 90 and s[i] <= 100 :
        count_su = count_su + 1
        
    if s[i] >= 80 and s[i] <= 89 :
        count_woo = count_woo + 1
        
    if s[i] >= 70 and s[i] <= 79 :
        count_mi = count_mi + 1  
        
    if s[i] >= 60 and s[i] <= 69 :
        count_yang = count_yang + 1 
        
    if s[i] >= 0 and s[i] <= 59 :
        count_ga = count_ga + 1
        
    i+=1
    
print("수 %d명 "% count_su)
print("우 %d명 "% count_woo)
print("미 %d명 "% count_mi)
print("양 %d명 "% count_yang)
print("가 %d명 "% count_ga)

결과값 

수 3명 
우 6명 
미 3명 
양 4명 
가 4명 

--------------------------------------------------

# 중첩리스트

numbers = [ [1,2,3,4,] , [5,6,7,8] ]

numbers[0] = [1,2,3,4] #numbers안의 리스트중 0번째 리스트

numbers[0][1] = 2 #numbers안의 리스트 중 0번째 리스트안의 1번째 숫자

--------------------------------------------------

# stack : First in Last Out (#처음 들어간게 마지막에 나옴)

li = ['mary','had','a','little','rabbit']
li.append('!')
li.pop( ), li.pop( ), li.pop( )

결과값 = ('!', 'rabbit', 'little')

# Queue : First In First Out (#처음 들어간게 처음에 나옴)
li = ['mary','had','a','little','rabbit']
li.pop( 0 ), li.pop( 0 ), li.pop( 0 )

--------------------------------------------------

#영화관 빈 좌석 표시하기

seats = [ [0,0,0,0,0,0,0,0,0,0],
         [0,0,0,0,0,0,0,0,0,0],
         [0,0,0,0,0,0,0,0,0,0],
         [1,1,1,0,0,0,0,0,1,0],
         [0,0,0,0,0,1,0,0,0,0],
         [0,1,0,0,0,1,0,1,0,0],
         [0,0,0,0,0,0,1,0,0,0],
         [1,0,1,0,0,0,0,0,0,1] ]

for i in range(len(seats)) : #seats안의 리스트 개수만큼
    for j in range(len(seats[i])) : #seats 안의 리스트 안의 요소의 개수만큼
        if seats[i][j] == 0 : #만약 i번째 리스트의 요소 j가 0이라면 (예약가능)
            print('%3s' % '□', end='') 
        else : #그 외 (예약 불가)
            print('%3s' % '■', end='')
    print()
    
print('\n ※예약 가능 : ■, 예약 불가 : □')

결과값 =

  □  □  □  □  □  □  □  □  □  □
  □  □  □  □  □  □  □  □  □  □
  □  □  □  □  □  □  □  □  □  □
  ■  ■  ■  □  □  □  □  □  ■  □
  □  □  □  □  □  ■  □  □  □  □
  □  ■  □  □  □  ■  □  ■  □  □
  □  □  □  □  □  □  ■  □  □  □
  ■  □  ■  □  □  □  □  □  □  ■

 ※예약 가능 : ■, 예약 불가 : □
 
--------------------------------------------------
 
 #흑돌백돌 표시
 
 stone = [[0,0,0,0,0,0,0,0,0],
         [0,1,0,1,2,1,2,1,0],
         [0,2,1,1,1,2,2,0,0],
         [0,0,2,2,2,1,0,2,0],
         [0,0,0,0,0,1,0,2,1],
         [0,0,0,2,0,1,2,1,0],
         [0,0,0,2,1,0,1,1,0],
         [0,0,0,1,1,0,0,0,0],
         [0,0,0,0,2,2,2,0,0],
        ]

jp = ["01","02","03","04","05","06","07","08","09"]

#0 - 돌 없음 , 1 - 흑돌 ,2 - 백돌

for i in range(len(stone)) :
    
    print(jp[i],end="")
    
    for j in range(len(stone[i])) :
       
        if stone[i][j] == 0 :
            print('%3s' % " Ｘ ",end = "")
        
        if stone[i][j] == 1 :
            print('%3s' % " ● ",end = "")
            
        if stone[i][j] == 2 :
            print('%3s' % " ○ ",end = "")
            
    
    print()

while 1 :

    x = int(input("X축 좌표값을 입력하세요(1~9, 종료시 -1 입력 : )"))
    
    if x == -1:    
        
        print("종료되었습니다!")
        
        break
   
    else :
        
        y = int(input("Y축 좌표값을 입력하세요(1~9, 종료시 -1 입력 : )"))
        
        if x <= 9 and y <= 9 :
    
            if stone[y-1][x-1] == 1 :    
                print("흑돌")

            if stone[y-1][x-1] == 2 :    
                print("백돌")

            if stone[y-1][x-1] == 0 :    
                print("돌없음")    
        else :
            print("숫자를 잘못입력하셨습니다. 다시 입력해 주세요")
