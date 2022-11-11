---
title: 字段MergingArgs
second_title: Aspose.Words for Java API 参考
description: 为 Merge字段 事件提供数据。
type: docs
weight: 218
url: /zh/java/com.aspose.words/fieldmergingargs/
---

**遗产:**
java.lang.Object, [com.aspose.words.字段MergingArgsBase](../../com.aspose.words/fieldmergingargsbase)
```
public class 字段MergingArgs extends 字段MergingArgsBase
```

提供数据为**Merge字段**事件。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

这**Merge字段**当在文档中遇到简单的邮件合并字段时，在邮件合并期间发生事件。您可以响应此事件以返回文本以供邮件合并引擎插入到文档中。
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
| [getText()](#getText--) | 获取将插入到当前合并字段的文档中的文本。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [set字段Value(Object value)](#set字段Value-java.lang.Object-) | 设置数据源中字段的值。 |
| [setText(String value)](#setText-java.lang.String-) | 为当前合并字段设置将插入到文档中的文本。 |
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
### getText() {#getText--}
```
public String getText()
```


获取将插入到当前合并字段的文档中的文本。

调用事件处理程序时，此属性设置为 null。

如果您将 Text 保留为 null，则邮件合并引擎将插入[字段MergingArgsBase.get字段Value()](../../com.aspose.words/fieldmergingargsbase\#get字段Value--) / [字段MergingArgsBase.set字段Value(java.lang.Object)](../../com.aspose.words/fieldmergingargsbase\#set字段Value-java.lang.Object-)代替合并字段。

如果将 Text 设置为任何字符串（包括空字符串），则该字符串将插入到文档中以代替合并字段。

**退货:**
java.lang.String - 将插入到当前合并字段的文档中的文本。
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

### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


为当前合并字段设置将插入到文档中的文本。

调用事件处理程序时，此属性设置为 null。

如果您将 Text 保留为 null，则邮件合并引擎将插入[字段MergingArgsBase.get字段Value()](../../com.aspose.words/fieldmergingargsbase\#get字段Value--) / [字段MergingArgsBase.set字段Value(java.lang.Object)](../../com.aspose.words/fieldmergingargsbase\#set字段Value-java.lang.Object-)代替合并字段。

如果将 Text 设置为任何字符串（包括空字符串），则该字符串将插入到文档中以代替合并字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 将插入到当前合并字段的文档中的文本。 |

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
