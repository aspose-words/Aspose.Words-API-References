---
title: DigitalSignatureCollection
second_title: Aspose.Words for Java API 参考
description: 提供附加到文档的数字签名的只读集合。
type: docs
weight: 112
url: /zh/java/com.aspose.words/digitalsignaturecollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public class DigitalSignatureCollection implements Iterable
```

提供附加到文档的数字签名的只读集合。

要了解更多信息，请访问**Work with Digital Signatures**文档文章。

[Document.getDigitalSignatures()](../../com.aspose.words/document\#getDigitalSignatures--)
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 获取指定索引处的文档签名。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 获取集合中包含的元素数。 |
| [hashCode()](#hashCode--) |  |
| [isValid()](#isValid--) | 如果此集合中的所有数字签名都有效并且文档未被篡改，则返回 true 如果没有数字签名，则返回 true。 |
| [iterator()](#iterator--) | 返回一个字典迭代器对象，该对象可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### get(int index) {#get-int-}
```
public DigitalSignature get(int index)
```


获取指定索引处的文档签名。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 签名的从零开始的索引。 |

**退货:**
[DigitalSignature](../../com.aspose.words/digitalsignature) - 指定索引处的文档签名。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCount() {#getCount--}
```
public int getCount()
```


获取集合中包含的元素数。

**退货:**
int - 集合中包含的元素数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isValid() {#isValid--}
```
public boolean isValid()
```


如果此集合中的所有数字签名都有效并且文档未被篡改，则返回 true 如果没有数字签名，则返回 true。如果至少一个数字签名无效，则返回 false。

**退货:**
布尔值 -\{ 如果此集合中的所有数字签名均有效且文档未被篡改，则返回 true 如果没有数字签名，则返回 true。
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个字典迭代器对象，该对象可用于迭代集合中的所有项目。

**退货:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
