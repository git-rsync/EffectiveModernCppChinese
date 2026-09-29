# 《Effective Modern C++ 》翻译
![bookLogo](http://p1.bpimg.com/567571/bc7c228ba08fae01.png)

> ！本书要求读者有较高水平的C++知识<br>
> ！条款后标注“已修订”表示该条款已经经过修订<br>
> ！全部译文同步自 [caochufeng/EffectiveModernCppChinese](https://gitee.com/caochufeng/EffectiveModernCppChinese)<br>

# 目录
0. [__简介__](./Introduction.md)
1. __类型推导__
	1. [Item 1:理解模板类型推导](./1.DeducingTypes/item1.md) 已修订
	2. [Item 2:理解auto类型推导](./1.DeducingTypes/item2.md)
	3. [Item 3:理解decltype](./1.DeducingTypes/item3.md)
	4. [Item 4:学会查看类型推导结果](./1.DeducingTypes/item4.md)
2. __auto__
	1. [Item 5:优先考虑auto而非显式类型声明](./2.Auto/item5.md)
	2. [Item 6:auto推导若非己愿，使用显式类型初始化惯用法](./2.Auto/item6.md)
3. __移步现代C++__
	1. [Item 7:区别使用()和{}创建对象](./3.MovingToModernCpp/item7.md) 已修订
	2. [Item 8:优先考虑nullptr而非0和NULL](./3.MovingToModernCpp/item8.md)
	3. [Item 9:优先考虑别名声明而非typedefs](./3.MovingToModernCpp/item9.md)
	4. [Item 10:优先考虑限域枚举而非未限域枚举](./3.MovingToModernCpp/item10.md) 已修订
	5. [Item 11:优先考虑使用deleted函数而非使用未定义的私有声明](./3.MovingToModernCpp/item11.md)
	6. [Item 12:使用override声明重载函数](./3.MovingToModernCpp/item12.md)
	7. [Item 13:优先考虑const_iterator而非iterator](./3.MovingToModernCpp/item13.md)
	8. [Item 14:如果函数不抛出异常请使用noexcept](./3.MovingToModernCpp/item14.md)
	9. [Item 15:尽可能的使用constexpr](./3.MovingToModernCpp/item15.md)
	10. [Item 16:让const成员函数线程安全](./3.MovingToModernCpp/item16.md)
	11. [Item 17:理解特殊成员函数的生成](./3.MovingToModernCpp/item17.md)
4. __智能指针__
	1. [Item 18:对于独占资源使用std::unique_ptr](./4.SmartPointers/item18.md)
	2. [Item 19:对于共享资源使用std::shared_ptr](./4.SmartPointers/item19.md) 已修订
	3. [Item 20:当std::shared_ptr可能悬空时使用std::weak_ptr](./4.SmartPointers/item20.md)
	4. [Item 21:优先考虑使用std::make_unique和std::make_shared，而非直接使用new](./4.SmartPointers/item21.md)
	5. [Item 22:当使用Pimpl惯用法，请在实现文件中定义特殊成员函数](./4.SmartPointers/item22.md)
5. __右值引用，移动语义，完美转发__
	1. [Item 23:理解std::move和std::forward](./5.RRefMovSemPerfForw/item23.md)
	2. [Item 24:区别通用引用和右值引用](./5.RRefMovSemPerfForw/item24.md)
	3. [Item 25:对于右值引用使用std::move，对于通用引用使用std::forward](./5.RRefMovSemPerfForw/item25.md)
	4. [Item 26:避免重载通用引用](./5.RRefMovSemPerfForw/item26.md)
	5. [Item 27:熟悉重载通用引用的替代品](./5.RRefMovSemPerfForw/item27.md)
	6. [Item 28:理解引用折叠](./5.RRefMovSemPerfForw/item28.md)
	7. [Item 29:认识移动操作的缺点](./5.RRefMovSemPerfForw/item29.md)
	8. [Item 30:熟悉完美转发失败的情况](./5.RRefMovSemPerfForw/item30.md)
6. __Lambda表达式__
	1. [Item 31:避免使用默认捕获模式](./6.LambdaExpressions/item31.md)
	2. [Item 32:使用初始化捕获来移动对象到闭包中](./6.LambdaExpressions/item32.md)
	3. [Item 33:对于std::forward的auto&&形参使用decltype](./6.LambdaExpressions/item33.md)
	4. [Item 34:优先考虑lambda表达式而非std::bind](./6.LambdaExpressions/item34.md)
7. __并发API__
	1. [Item 35:优先考虑基于任务的编程而非基于线程的编程](./7.TheConcurrencyAPI/Item35.md)
	2. [Item 36:如果有异步的必要请指定std::launch::async](./7.TheConcurrencyAPI/item36.md)
	3. [Item 37:从各个方面使得std::threads unjoinable](./7.TheConcurrencyAPI/item37.md)
	4. [Item 38:关注不同线程句柄析构行为](./7.TheConcurrencyAPI/item38.md)
	5. [Item 39:考虑对于单次事件通信使用void](./7.TheConcurrencyAPI/item39.md)
	6. [Item 40:对于并发使用std::atomic，volatile用于特殊内存区](./7.TheConcurrencyAPI/item40.md)
8. __微调__
	1. [Item 41:对于那些可移动总是被拷贝的形参使用传值方式](./8.Tweaks/item41.md)
	2. [Item 42:考虑就地创建而非插入](./8.Tweaks/item42.md)

## 翻译相关
+ constness译为常量性，volatitleness译为易变性，reference-ness视情况直接译为引用
+ built-in译为内置而不是内建
+ literal译为字面值
+ 诚恳接受typo-pull-request以及错译pr
+ 我蒟多线程方面(7.)基础薄弱，所幸译前还有大量时间进行知识储备
+ 翻译到后面我觉得要想坚持不写译注几乎不可能，所以译注将会以_[num]_标出，详细内容将会出现在文末。
+ :)

## 免责声明
译者纯粹出于学习目的与个人兴趣翻译本书，不追求任何经济利益。译者保留对此版本译文的署名权，其他权利以原作者和出版社的主张为准。本译文只供学习研究参考之用，不得公开传播发行或用于商业用途。有能力阅读英文书籍者请购买正版支持。
