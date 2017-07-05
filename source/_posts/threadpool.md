---
title: java集合框架
date: 2017-01-02 12:20:00
---
## java集合框架体系
java集合框架大致分为List、Set和Map，List表示有序可重复集合，Set表示无序不可重复集合，Map表示有映射关系的集合。java 1.5之后添加了Queue接口，表示为队列集合。
## java集合框架继承图
![继承图](/images/java_collection.png)
## Collection
Collection是List、Set和Queue接口的父接口。
Collection接口定义的方法(jdk1.7)：
```java
int size();//集合元素数量
boolean isEmpty();//是否为空集合
boolean contains(Object o);//是否包含某个对象
Object[] toArray();//转换为数组
<T> T[] toArray(T[] a);//如果数组a长度小于集合大小，就会根据泛型新建一个数组，然后将集合元素放在数组a中并返回
boolean add(E e);//添加一个元素
boolean remove(Object o);//移除某个元素
boolean containsAll(Collection<?> c);//是否包含c集合的所有元素
boolean addAll(Collection<? extends E> c);//添加一个集合
boolean removeAll(Collection<?> c);//移除包含在c集合中的元素，即取两个集合的差集
boolean retainAll(Collection<?> c);//移除不包含在c集合中的元素，即取两个集合的交集
void clear();//清除元素
boolean equals(Object o);
int hashCode();
```
## AbstractCollection
AbstractCollection是一个抽象类，子类可以继承AbstractCollection选择要实现的方法，而不必实现Collection所有方法。
AbstractCollection只有两个抽象方法：
```java
public abstract Iterator<E> iterator();
public abstract int size();
```
