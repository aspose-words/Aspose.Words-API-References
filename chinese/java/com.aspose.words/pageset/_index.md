---
title: PageSet
second_title: Aspose.Words for Java API 参考
description: 描述一组随机页面。
type: docs
weight: 439
url: /zh/java/com.aspose.words/pageset/
---

**遗产：**
java.lang.Object
```
public class PageSet
```

描述一组随机页面。

要了解更多信息，请访问**Programming with Documents**文档文章。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [PageSet(int page)](#PageSet-int-) | 根据确切的页面索引创建单页集。 |
| [PageSet(int[] pages)](#PageSet-int...-) | 根据确切的页面索引创建页面集。 |
| [PageSet(PageRange[] ranges)](#PageSet-com.aspose.words.PageRange...-) | 根据范围创建页面集。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAll()](#getAll--) | 获取文档所有页面按原始顺序排列的集合。 |
| [getClass()](#getClass--) |  |
| [getEven()](#getEven--) | 获取文档的所有偶数页按其原始顺序排列的集合。 |
| [getOdd()](#getOdd--) | 获取文档的所有奇数页按其原始顺序排列的集合。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PageSet(int page) {#PageSet-int-}
```
public PageSet(int page)
```


根据确切的页面索引创建单页集。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| page | int | 页面的从零开始的索引。如果遇到不在文档中的页面，渲染时会抛出异常。表示文档中的最后一页。 |

### PageSet(int[] pages) {#PageSet-int...-}
```
public PageSet(int[] pages)
```


根据确切的页面索引创建页面集。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pages | int[] | 从零开始的页面索引。如果遇到不在文档中的页面，渲染时会抛出异常。表示文档中的最后一页。 |

### PageSet(PageRange[] ranges) {#PageSet-com.aspose.words.PageRange...-}
```
public PageSet(PageRange[] ranges)
```


根据范围创建页面集。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ranges | [PageRange\[\]](../../com.aspose.words/pagerange) | 页面范围数组。如果遇到从文档最后一页之后开始的范围，则在渲染过程中会抛出异常。在最后一页之后结束的所有范围都将被截断以适合文档。 |

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getAll() {#getAll--}
```
public static PageSet getAll()
```


获取文档所有页面按原始顺序排列的集合。

**退货：**
[PageSet](../../com.aspose.words/pageset) - 一组按原始顺序排列的文档的所有页面。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getEven() {#getEven--}
```
public static PageSet getEven()
```


获取文档的所有偶数页按其原始顺序排列的集合。由于页面索引是从零开始的，因此偶数页具有奇数索引。

**退货：**
[PageSet](../../com.aspose.words/pageset) - 文档的所有偶数页均按原始顺序排列的集合。
### getOdd() {#getOdd--}
```
public static PageSet getOdd()
```


获取文档的所有奇数页按其原始顺序排列的集合。奇数页具有偶数索引，因为页面索引是从零开始的。

**退货：**
[PageSet](../../com.aspose.words/pageset) - 一组按原始顺序排列的文档的所有奇数页。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
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




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
