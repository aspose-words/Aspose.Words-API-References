---
title: FieldMergingArgsBase
second_title: Aspose.Words for Java API 参考
description: 和 的基类。
type: docs
weight: 219
url: /zh/java/com.aspose.words/fieldmergingargsbase/
---

**遗产：**
java.lang.Object
```
public abstract class FieldMergingArgsBase
```

基类为[FieldMergingArgs](../../com.aspose.words/fieldmergingargs)和[ImageFieldMergingArgs](../../com.aspose.words/imagefieldmergingargs).

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [FieldMergingArgsBase()](#FieldMergingArgsBase--) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | 返回[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。 |
| [getDocumentFieldName()](#getDocumentFieldName--) | 获取文档中指定的合并字段的名称。 |
| [getField()](#getField--) | 获取表示当前合并字段的对象。 |
| [getFieldName()](#getFieldName--) | 获取数据源中合并字段的名称。 |
| [getFieldValue()](#getFieldValue--) | 从数据源中获取字段的值。 |
| [getRecordIndex()](#getRecordIndex--) | 获取正在合并的记录的从零开始的索引。 |
| [getTableName()](#getTableName--) | 获取当前合并操作的数据表的名称，如果名称不可用，则为空字符串。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object-) | 设置来自数据源的字段值。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FieldMergingArgsBase() {#FieldMergingArgsBase--}
```
public FieldMergingArgsBase()
```


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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDocument() {#getDocument--}
```
public Document getDocument()
```


返回[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。

**退货：**
[Document](../../com.aspose.words/document) - 这[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。
### getDocumentFieldName() {#getDocumentFieldName--}
```
public String getDocumentFieldName()
```


获取文档中指定的合并字段的名称。

如果您有从文档字段名称到不同数据源字段名称的映射，那么这是文档中指定的原始字段名称。

如果您在文档中指定了字段名称前缀，例如“Image:MyFieldName”，则**DocumentFieldName**返回不带前缀的字段名称，即“MyFieldName”。

**退货：**
java.lang.String - 文档中指定的合并字段的名称。
### getField() {#getField--}
```
public FieldMergeField getField()
```


获取表示当前合并字段的对象。

**退货：**
[FieldMergeField](../../com.aspose.words/fieldmergefield) - 表示当前合并字段的对象。
### getFieldName() {#getFieldName--}
```
public String getFieldName()
```


获取数据源中合并字段的名称。

如果您有从文档字段名称到不同数据源字段名称的映射，那么这就是映射的字段名称。

如果您在文档中指定了字段名称前缀，例如“Image:MyFieldName”，则**FieldName**返回不带前缀的字段名称，即“MyFieldName”。

**退货：**
java.lang.String - 数据源中合并字段的名称。
### getFieldValue() {#getFieldValue--}
```
public Object getFieldValue()
```


从数据源中获取字段的值。此属性包含邮件合并引擎刚刚从您的数据源中为该字段选择的值。您还可以通过设置属性来替换值。

**退货：**
java.lang.Object - 来自数据源的字段值。
### getRecordIndex() {#getRecordIndex--}
```
public int getRecordIndex()
```


获取正在合并的记录的从零开始的索引。

**退货：**
int - 正在合并的记录的从零开始的索引。
### getTableName() {#getTableName--}
```
public String getTableName()
```


获取当前合并操作的数据表的名称，如果名称不可用，则为空字符串。

**退货：**
java.lang.String - 当前合并操作的数据表名称，如果名称不可用，则为空字符串。
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




### setFieldValue(Object value) {#setFieldValue-java.lang.Object-}
```
public void setFieldValue(Object value)
```


设置来自数据源的字段值。此属性包含邮件合并引擎刚刚从您的数据源中为该字段选择的值。您还可以通过设置属性来替换值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.Object | 来自数据源的字段值。 |

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
