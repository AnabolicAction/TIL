# Ruby

### 0.개요

1. 루비는 순수 객체지향 언어이다.
2. 모든것이 객체
3. Ruby on Rails 프레임 워크 등장으로 유명
4. 주석처리 #

### 1.puts vs print

~~~ruby
3.times{print "hellow"} #=> hellohellohello
3.times{puts "hellow"} #=> hello
						 hello
						 hello
~~~

- puts는 개행문자 포함

### 2. p vs puts

~~~ruby
string = "hello"
puts string #=> hello => nul
p string #"hello"=>"hello"
~~~

### 3. Naming conventions

- 변수
  - snake case
- 상수
  - CONSTANT
- 클래스
  - CamelCase

### 4. pry

- 설치

  - `gem install pry`

- 실행

  - pry

  

### 5. inline statement

~~~ruby
#if 문
pry(main)> puts "a=0" if a==0 #"a=0"
pry(main)> puts "a=0" if a==1 #출력안됨
#while 문
pry(main)> c=2
 pry(main)> result = c+=2 while c<50 
    puts result#50
 puts "hi" if 0 #if 0=true
     #hi
~~~

### 6. case

~~~ruby
case name
when "taewoo" then puts "hi taewoo"  
when "lee" then puts "hi lee"  
else puts "get out!!"  
end  
~~~

### 7.method

- 대부분의 언어
  - 클래스 밖 :function
  - 클래스 안:method
  - 