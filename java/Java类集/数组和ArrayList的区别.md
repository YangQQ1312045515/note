联系：

- ArrayList的底层数据结构就是数组：Object[]，如`ArrayList.add : element[size++] = e`
- 两者都可以随机访问，并且时间复杂度都是O(1)



区别：

- 创建数组时必须指定数组大小，且不需要泛型指定
- ArrayList创建时无需指定大小，该类可以自动扩容，每次扩容为原来的1.5倍
- 数组可以是多维的，ArrayList只能是一维



# HashMap

JDKK 1.8以前HashMap采用数组的方式实现，哈希冲突采用拉链法

如果数据是连续的，那么哈希算法可以采用一个一元一次函数。。。保证了不冲突效率也高。key是x，存储位置是y

JDK以后当链表的长度大于8时就会变成红黑树来处理哈希冲突