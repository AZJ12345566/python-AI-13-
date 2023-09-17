# python-AI-13-
python+AI笔记(13)
# 一阶-六章-字符串的课后练习讲解
my_str="bala cala dala"
num=my_str.count("la")
print(num)
new_my_str.replace(" ","|")
print(new_my_str)
my_str_list=new_my_str.split("|")
print(my_str_list)

# 一阶-六章数据容器(序列)的切片
#序列是指:内容连续、有序，可使用下标索引的一类数据容器
#列表、元组、字符串均可以视为序列
#次操作不会影响序列本身，而是会得到一个新的序列
my_list=[0,1,2,3,4,5,6]
result1=my_list[1:4:1]  #步长默认是1
print(result1)

my_tuple=(0,1,2,3,4,5,6)
result2=my_tuple[:]  #起始和结束表示从头到尾
print(result2)

my_str="01234567"
result3=my_str[::2]
print(result3)

my_str="01234567"
result4=my_str[::-1]  #等同于将序列反转了
print(result4)  #输出为76543210

my_list=[0,1,2,3,4,5,6]
result5=my_list=[3:1:-1]
print(result5)

my_tuple=(0,1,2,3,4,5,6)
result6=my_tuple[::-2]
print(result6)  #输出为6,4,2,0

# 一阶-六章-序列的切片课后练习讲解
my_str="bala 员序程 "
result1=my_str[::-1][0:3]
print(result1)
#切片取出，然后倒序
result2=my_str[5:8][::-1]
print(result2)
#split分隔"."replace替换"来"为空，倒序字符串
result3=my_str.split(" ")[1].replace("员","")[::-1]
print(result3) #输出程序
# 一阶-六章-集合的定义和操作
#集合与其他学习的三种元素最大的不同是不支持元素的重复、并且内容无序
#集合通过{}来定义
my_set={"bala","cala","dala","bala","cala","dala","bala","cala","dala"}
my_set_empty=set()  #定义空集合
print(f"my_set的内容是:{my_set},类型是:{type(my_set)}")
print(f"my_set_empty的内容是:{my_set_empty},类型是:{type(my_set_empty)}")
#以上输出自动取出重复内容。同时集合的元素顺序是无法保证的，因此下标索引是无法支持访问的
#但是集合和列表一样，是允许修改的
my_set.add("Python")
my_set.add("bala")  #这里添加相同的元素是无法生效的，会被自动去重的
print(f"my_set添加元素后的结果是:{my_set}")

#移除元素
my_set.remove("bala")
print(f"my_set移除bala后，结果是:{my_set}")

#随机取出一个元素
my_set={"bala","cala","dala",}
element=my_set.pop()  #这里和列表的pop的区别是，这里不能指定取出元素的下标，因为他是无序的，下标是不固定的
print(f"集合被取出元素是:{element},取出元素后:{my_set}")


#清空集合
my_set.clear()
print(f"集合被清空了，结果是:{my_set}")  #输出set()

#取出2个集合的差集
set1={1,2,3}
set2={1,5,6}
set1.difference(set2)  #找差集是找出集合1有的集合2没有的
print(f"取出差集后的结果是:{set3}")
print(f"取出差集后，原有set1的内容:{set1}")
print(f"取出差集后，原有set2的内容:{set2}")  #原有的集合是不会变的

#在集合1中消除集合的差集
set1={1,2,3}
set2={1,5,6}
set1.difference_update(set2)
print(set1)  #输出{2,3}
print(set2)  #输出{1,5,6}

#两个集合合并成一个集合
set1={1,2,3}
set2={1,5,6}
set3=set1.union(set2)
print(set3)  #输出{1,2,3,5,6}
print(set1)  #以下输出原来的集合
print(set2)

#统计集合元素数量len()
set{1,2,3,4,5}
num=len(set1)
print(num)  #输出重复的也是5个

#集合的遍历
#集合不支持下标索引，所以不能用while循环
#可以用for循环
set1={1,2,3,4,5}
for element in set1:
    print(element)

# 一阶-六章-集合的课后练习
my_list=['bala','cala','bala','cala','dala','fala','dala','fala','best']
my_set=set()
for element in my_list:
    my_set.add(element)
print(my_list)
print(my_set)
