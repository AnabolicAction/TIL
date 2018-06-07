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
- 루비에서는 모든 function은 method

~~~ruby
#루비에서의 method 선언
def simple
 puts "simple!!"
 end  
=> :simple
def asdf()
 puts "asdf"
 end  
=> :asdf
~~~

- ~~~ruby
  #루비에서는 return이 없을때 마지막 연산 값을 return 합니다
   def add2(a,b)
   a+b
  end  
  => :add2
  add2(1,2)
  => 3
  #루비에서는 return을 선택적으로 사용가능
  def divide(a,b)
   return "I don't think so" if b==0
   a/b
  end
  divide(4,0)
  ~~~

- 기본 매개변수

- ~~~ruby
  def factorial(n)
      n==0 ? 1:n*factorial(n-1)
  end
  factoral #ArgumentError: wrong number of arguments (given 0, expected 1)
  def factorial_d(n=5)
      n==0 ? 1:n*factorial_d(n-1)
  end
  facrtoral_d #120
  ~~~

### 8.block

~~~ruby
#완벽하게 같은 문장입니다
3.times {puts "hello"}

3.times do |asdf|
puts asdf #요부분이 block 입니다.
 end  

~~~

~~~ruby
def hihi
	return "no block" unless block_given?
	yield
end  
hihi 
#=> "no block"
hihi{puts "hihi"}
#hihi
~~~

### 9.string

~~~ruby
name ="taewoo"
=> "taewoo"
a="#{name}님 안녕하소"                             
#"taewoo님 안녕하소"

b='#{name}님 안녕하소'
#"\#{name}님 안녕하소
~~~

~~~ruby
my_name="taewoo"
#=> "taewoo"
 my_name.upcase! #!붙이면 객체를 바꿔서 저장
#=> "TAEWOO"
 my_name
#=> "TAEWOO"
~~~

### 10.hash

- key,value로 이루어져있다!!

  ~~~ruby
  hash1 ={:key => value}
  hash2 = {key: value} #key와 :붙어있어야함
  hash3 = {"key" => value}
  ~~~

- each 반복하기

  ~~~ruby
  hash1.each do|k,v|  # k,v는 어떠한 문자도 적어도됨                puts "#{k}:#{v}"  
   end  
  ~~~

  

### 