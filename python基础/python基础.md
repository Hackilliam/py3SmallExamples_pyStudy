Jupyter Notebook运行文件python基础.ipynb

### ---------------------------------------------------------------------------------------------------------------

python基础主要总结python常用内置函数；python独有语法特性、关键词nonlocal、global等；内置数据结构包括：列表(list)、字典(dict)、集合(set)、元组(tuple)以及相关的高级模块collections中的Counter、namedtuple、defaultdict、heapq模块。

1.求绝对值

​		abs(-6)

2.元素都为真

​		接受一个迭代器，如果迭代器的所有元素都为真，则返回True，否则False

​		all([1,0,3,6])

​		all([1,2,3])

3.元素至少一个为真

​		接受一个迭代器，如果迭代器里至少有一个元素为真，则返回True,否则False

​		any([0,0,0,[]])

​		any([0,0,1])

4.ascii展示对象

​		调用对象的repr()方法，获得该方法的返回值

​		class Student():

​				def __ init __(self,id,name):

​						self.id=id

​						self.name=name

​				def __ repr __(self):

​						return 'id='+self.id+',name='+self.name

​		xiaoming=Student(id='001',name='xiaoming')

​		print(xiaoming)

​		ascii(xiaoming)

5.十转二、十转八、十转十六

​		bin(10)

​		oct(9)

​		hex(15)

6.判断是真是假

​		bool([0,0,0])

​		bool([])

​		bool([1,0,1])

7.字符串转成字节

​		s="apple"

​		bytes(s,encoding='utf-8')

8.转为字符串

​		i=100

​		str(i)

9.是否可被调用

​		能被调用的对象就是一个callable对象，比如函数str,int等都是可以被调用的

​		callable(str)

​		callable(int)

​		xiaoming

​		callable(xiaoming)

​		如果需要让xiaoming能被调用xiaoming()，需要重写Student类的__ call __方法：

​		class Student():

​				def __ init __(self,id,name):

​						self.id=id

​						self.name=name

​				def __ repr __(self):

​						return 'id='+self.id+',name='+self.name

​				def __ call __(self):

​						print('I can be called.')

​						print(f'my name is {self.name}')

​				t=Student('001','xiaoming')

​				t();

### ---------------------------------------------------------------------------------------------------------------

额外记录：

​		print、repr和str的区别：

​				print：将对象打印输出，输出的结果无类型

​				repr：用于将对象转化为可供解释器读取的字符串形式

​				str：用于将对象转化为适于人阅读的字符串形式

​		