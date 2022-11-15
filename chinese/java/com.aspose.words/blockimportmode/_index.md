---
title: BlockImportMode
second_title: Aspose.Words for Java API 参考
description: 指定如何从基于 HTML 的文档中导入块级元素的属性。
type: docs
weight: 29
url: /zh/java/com.aspose.words/blockimportmode/
---

**遗产:**
java.lang.Object
```
public class BlockImportMode
```

指定如何从基于 HTML 的文档中导入块级元素的属性。
## 字段

| 场地 | 描述 |
| --- | --- |
| [MERGE](#MERGE) | 父块的属性被合并并存储在子元素上（即 |
| [PRESERVE](#PRESERVE) | 父块的属性被导入到一个特殊的逻辑结构中，并与文档节点分开存储。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String blockImportModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int blockImportMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int blockImportMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


父块的属性被合并并存储在子元素（即段落或表格）上。

父块的属性合并如下：边距加在一起；高层块的边界被丢弃，只保留最内层的边界。因此，当指定此模式时，原始文档中块的某些格式将丢失。

另一方面，由于所有合并的块级属性都存储在文档节点上，因此生成的文档中的所有格式都可用于修改。

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


父块的属性被导入到一个特殊的逻辑结构中，并与文档节点分开存储。

仅导入“body”、“div”和“blockquote”HTML 元素的边距和边框。每个 HTML 元素的属性都是单独存储的。

此模式允许更好地保留在 HTML 文档中看到的边框和边距，并获得更好的转换结果。缺点是生成的文档更难修改，因为存储在逻辑结构中的边框和边距不可用于编辑。

此模式模仿 MS Word 关于块属性导入的行为。

### length {#length}
```
public static int length
```


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
### fromName(String blockImportModeName) {#fromName-java.lang.String-}
```
public static int fromName(String blockImportModeName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int blockImportMode) {#getName-int-}
```
public static String getName(int blockImportMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| blockImportMode | int |  |

**退货:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货:**
整数[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
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




**退货:**
java.lang.String
### toString(int blockImportMode) {#toString-int-}
```
public static String toString(int blockImportMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| blockImportMode | int |  |

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
