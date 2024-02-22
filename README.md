# PythonSutdy
a = "Life is too short, You need Python"
print(a[3])
print(a[12])
print(a[-1])


#59p 슬라이싱 기법 , 공백 문자도 문자로 취
a = "Life is too short, You need Python"
print(a[0:4])

# a[시작_번호:끝_번호]에서 끝 번호 부분 생략하면 시작번호부터 끝까지 뽑아낸다.
print(a[19:])
# a[시작_번호:끝_번호]에서 시작번호를 생략하면 문자열의 처음부터 끝번호까지 뽑아낸다.
print(a[:17])
# a[시작_번호:끝_번호]에서 시작 번호와 끝 번호를 생략하면 문자열의 처음부터 끝까지 뽑아낸다.
print(a[:])
# 슬라이싱에서도 인덱싱과 마찬가지로 -(빼기)기호를 사용할 수 있다.
print(a[19:-7])

# 62p a[1] = 'y'로 선언하면 오류가 발생하므로슬라이싱을 사용해야 한다.
a = "Pithon"
print('\n'+ a);
print(a[:1])
print(a[2:])

a =a[:1] + 'y' + a[2:]
print(a + "\n")

# 62p 문자열 포메팅
# 1.숫자 바로 대입
print( "I eat %d apples." % 3 )

# 2.문자열 바로 대입
print( "I eat %s applies." % "five"+"\n")
# 3. 숫자 값을 나타내는 변수로 대입
number = 3
print("I eat %d applies." % number +"\n")
# 4. 2개 이상의 값 넣기
number = 10
day = "three"
print("I ate %d apples. so I was sick for %s days." % (number, day) +"\n")

# %s 포멧 코드는 모든 형태의 값이든 변환해 넣을 수 있다.
# 원래 %d나 %f를 사용해야 하지만 %s를 사용하면 괜찮다.

#포매팅 연산자 %d와 %를 같이 쓸 때는 %%를 쓴다. %d%는 오류 %d%%로 사용 (%d와 같은 포메팅 연산자가 없으면 %는 홀로 쓰여도상관없다)
print("Error is %d%%." % 98 )

# 1. 정렬과 공백 %10s는 전체 길이가 10개인 문자열 공간에서 대입되는 값을 오른쪽으로 정렬하고 그 앞의 나머지는 공백으로 남겨둔다.
print("%10s" % "hi" )   # hi가 오른쪽 정렬
print("%-10sjane." % 'hi')# hi가 왼쪽 정렬
# 2. 소수점 표현하기
print("%0.4f \n" % 3.42134234)

#67p format함수를 사용한 포매팅 
print( "I eat {0} apples \n".format(3) )# 숫자 바로 대입하기
print( "I eat {0} apples \n".format("five") )#문자열 바로 대입하
number = 3
print( "I eat {0} apples \n".format(number) )
number = 10
day = "three"
print( "I ate {0} apples. so I was sick for {1} days. ".format(number, day) )# 2개 이상의 값 넣
print( "I ate {number} apples. so I was sick for {day} days.".format(number=10, day=3) ) #이름으로 넣기
print( "I ate {0} apples. so I was sick for {day} days. \n".format(10, day=3) ) # 인덱스와 이름을 혼용해서 넣기
print( "{0:<10}_".format("hi") ) # 왼쪽10정렬
print( "{0:>10}_".format("hi") ) # 오른쪽10 정렬
print( "{0:^10}_".format("hi") ) # 가운데 정렬
print( "{0:=^10}".format("hi") ) # 공백 채우기
print( "{0:!<10}".format("hi") )
y = 3.42134234
print( "{0:10.4f}".format(y) )# 10정렬
# {또는} 문자 표현하기
print("{{ and }} \n".format() ) # {}문자 표현하기
# f문자열 포매팅은 3.6버전부터 사용 가능

print( "# 72p 문자열 관련 함수")
a = "hobby"
print(a.count('b') ) # 문자 개수 세기 -count

a = "Python is the best choice" # 위치 알려 주기 1 -find
print( a.find('b') )
print( a.find('k') )

a = "Life is too short" # 위치 알려 주기 2
print( a.index('t') )
# print( a.index('k') )

print( ",".join('abcd') ) # 문자열 삽입 join
print( ",".join(['a', 'b', 'c', 'd']) )

a = "hi"
print(a.upper() ) # 소문자를 대문자로 바꾸기 
a = "HI"
print(a.lower() ) # 대문자를 소문자로 바꾸기
# 75p 부터 나중에 더 작성하기

print("# 리스트 자료형 77p ")
#a[-1]은 문자 열에서와 마찬가지로 리스트 a의 마지막 요솟값을 말한다.
a= [1, 2, 3, ['a', 'b', 'c']]
print( a[-1] )
print( a[-1][0]) # 이중 리스트
print( a[0:2] ) # 리스트슬라이싱

a = [1, 2, 3, 4, 5]
b = a[:2]
c = a[2:]
print("\n", a );
print( b  ) # 처음부터 a[1]까지
print( c) # a[2]부터 마지막까지

print("중첩된 리스트에서 슬라이싱하기")
a = [1, 2, 3, ['a', 'b', 'c'], 4, 5]
print(a[2:5])
print(a[3][:2])

#리스트 연산하기
a = [1,2,3]
b = [4,5,6]
print(a + b)
print(a * 3)
print( len(a) ) # 리스트 길이 구하기

# 정수와 문자열을 더하면 오류생긴다. str()선언해야한다.
print( str(a[2]) + "hi" )

print("리스트의 수정과 삭제")
a = [1, 2, 3]
a[2] = 4
print(a) # 리스트의 값 수정
a = [1, 2, 3]
del a[1]
print(a) # del함수를 사용해 리스트 요소 삭제
a = [1, 2, 3, 4, 5]
del a[2:]
print(a) # a[2]부터 끝까지 삭제

print("리스트 관련 함수 84p")
a = [1,2,3]
a.append(4) # 리스트의 맨 마지막에 4를 추가
print(a)
#리스트 안에 다시 리스트를 추가할 수있다.
a.append([5, 6]) # 리스트의 맨 마지막이 [5,6]을 추
print(a)

<br>
0222<br>
aws a#650<br>

재고 게시판<br>
검색 수정 삭제 추가<br>
aws는 무료 서버준다.<br>
파이썬 취업처 없음<br>
연동은 파이썬으로 한다.<br>
★★★ 파이선교재 시작<br>
★설치시 Add python.exe to Path 반드시 체크해라<br>
3.117 64BIT 다운로드<br>

ctrl + z로 나올수 있음<br>
들여쓰기4칸(tap)<br>
인텔리제이 나중에 사용<br>
튜플 89p ,93p 딕셔너리, 집합자료형, bool자료형,input<br>
183p import sys<br>
● 웹크롤링: 웹페이지 분석해서 내 DB에 넣는거 <br>
pyton.posStem분석하기<br>
10-2에다 붙이고 main 더블클릭하면 실해된다.<br>
주석 달아서 캡처후 시험봄<br>
크롤링할때 파이썬사용<br>
idle<br>
