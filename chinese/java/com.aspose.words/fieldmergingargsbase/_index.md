---
title: 字段MergingArgsBase
second_title: Aspose.Words for Java API 参考
description:和 的基类。
type: docs
weight: 219
url: /zh/java/com.aspose.words/fieldmergingargsbase/
---

**遗产:**
java.lang.Object
```
public abstract class 字段MergingArgsBase
```

基类[字段MergingArgs](../../com.aspose.words/fieldmergingargs)和[Image字段MergingArgs](../../com.aspose.words/imagefieldmergingargs).

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [字段MergingArgsBase()](#字段MergingArgsBase--) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDocument()](#getDocument--) | 返回[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。 |
| [getDocument字段Name()](#getDocument字段Name--) | 获取文档中指定的合并字段的名称。 |
| [get字段()](#get字段--) | 获取表示当前合并字段的对象。 |
| [get字段Name()](#get字段Name--) | 获取数据源中合并字段的名称。 |
| [get字段Value()](#get字段Value--) | 从数据源获取字段的值。 |
| [getRecordIndex()](#getRecordIndex--) | 获取正在合并的记录的从零开始的索引。 |
| [getTableName()](#getTableName--) | 获取当前合并操作的数据表的名称，如果名称不可用，则为空字符串。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [set字段Value(Object value)](#set字段Value-java.lang.Object-) | 设置数据源中字段的值。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### 字段MergingArgsBase() {#字段MergingArgsBase--}
```
public 字段MergingArgsBase()
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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDocument() {#getDocument--}
```
public Document getDocument()
```


返回[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。

**退货:**
[Document](../../com.aspose.words/document) - 这[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。
### getDocument字段Name() {#getDocument字段Name--}
```
public String getDocument字段Name()
```


获取文档中指定的合并字段的名称。

如果您有从文档字段名称到不同数据源字段名称的映射，则这是文档中指定的原始字段名称。

如果您在文档中指定了字段名称前缀，例如“Image:My字段Name”，则**Document字段Name**返回不带前缀的字段名称，即“My字段Name”。

**退货:**
java.lang.String - 文档中指定的合并字段的名称。
### get字段() {#get字段--}
```
public 字段Merge字段 get字段()
```


获取表示当前合并字段的对象。

**退货:**
[字段Merge字段](../../com.aspose.words/fieldmergefield) - 表示当前合并字段的对象。
### get字段Name() {#get字段Name--}
```
public String get字段Name()
```


获取数据源中合并字段的名称。

如果您有从文档字段名称到不同数据源字段名称的映射，那么这就是映射的字段名称。

如果您在文档中指定了字段名称前缀，例如“Image:My字段Name”，则**字段Name**返回不带前缀的字段名称，即“My字段Name”。

**退货:**
java.lang.String - 数据源中合并字段的名称。
### get字段Value() {#get字段Value--}
```
public Object get字段Value()
```


从数据源获取字段的值。此属性包含邮件合并引擎刚刚从您的数据源中为此字段选择的值。您还可以通过设置属性来替换该值。

**退货:**
java.lang.Object - 数据源中的字段值。
### getRecordIndex() {#getRecordIndex--}
```
public int getRecordIndex()
```


获取正在合并的记录的从零开始的索引。

**退货:**
int - 正在合并的记录的从零开始的索引。
### getTableName() {#getTableName--}
```
public String getTableName()
```


获取当前合并操作的数据表的名称，如果名称不可用，则为空字符串。

**退货:**
java.lang.String - 当前合并操作的数据表的名称，如果名称不可用，则为空字符串。
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




### set字段Value(Object value) {#set字段Value-java.lang.Object-}
```
public void set字段Value(Object value)
```


设置数据源中字段的值。此属性包含邮件合并引擎刚刚从您的数据源中为此字段选择的值。您还可以通过设置属性来替换该值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.Object | 数据源中的字段值。 |

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
