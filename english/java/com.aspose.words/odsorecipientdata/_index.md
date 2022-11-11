---
title: OdsoRecipientData
second_title: Aspose.Words for Java API 参考
description: 表示有关要从邮件合并中排除的外部数据源中的单个记录的信息。
type: docs
weight: 416
url: /zh/java/com.aspose.words/odsorecipientdata/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

表示有关要从邮件合并中排除的外部数据源中的单个记录的信息。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

如果将记录合并到合并文档中，则不需要有关该记录的信息。但是，如果给定记录不应合并到合并文档中，则该记录的唯一键值应存储在[getUniqueTag()](../../com.aspose.words/odsorecipientdata\#getUniqueTag--) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata\#setUniqueTag-byte---)此对象的属性以指示此排除。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [deepClone()](#deepClone--) | 返回此对象的深层克隆。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getActive()](#getActive--) | 指定在执行邮件合并时是否应将来自数据源的记录导入到文档中。 |
| [get班级()](#get班级--) |  |
| [getColumn()](#getColumn--) | 指定数据源中包含当前记录的唯一数据的列。 |
| [getHash()](#getHash--) | 表示此记录的哈希码。 |
| [getUniqueTag()](#getUniqueTag--) | 指定包含唯一数据的列中给定记录的内容。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setActive(boolean value)](#setActive-boolean-) | 指定在执行邮件合并时是否应将来自数据源的记录导入到文档中。 |
| [setColumn(int value)](#setColumn-int-) | 指定数据源中包含当前记录的唯一数据的列。 |
| [setHash(int value)](#setHash-int-) | 表示此记录的哈希码。 |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte---) | 指定包含唯一数据的列中给定记录的内容。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public OdsoRecipientData deepClone()
```


返回此对象的深层克隆。

**退货:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata)
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
### getActive() {#getActive--}
```
public boolean getActive()
```


指定在执行邮件合并时是否应将来自数据源的记录导入到文档中。默认值是true 。

**退货:**
boolean - 对应的布尔值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getColumn() {#getColumn--}
```
public int getColumn()
```


指定数据源中包含当前记录的唯一数据的列。默认值为 0。

**退货:**
int - 对应的 int 值。
### getHash() {#getHash--}
```
public int getHash()
```


表示此记录的哈希码。有时 Microsoft Word 使用[getHash()](../../com.aspose.words/odsorecipientdata\#getHash--) / [setHash(int)](../../com.aspose.words/odsorecipientdata\#setHash-int-)整条记录而不是[getUniqueTag()](../../com.aspose.words/odsorecipientdata\#getUniqueTag--) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata\#setUniqueTag-byte---)价值。默认值为 0。

**退货:**
int - 对应的 int 值。
### getUniqueTag() {#getUniqueTag--}
```
public byte[] getUniqueTag()
```


指定包含唯一数据的列中给定记录的内容。默认值为 null 。

**退货:**
字节[- 对应的字节[] 价值。
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




### setActive(boolean value) {#setActive-boolean-}
```
public void setActive(boolean value)
```


指定在执行邮件合并时是否应将来自数据源的记录导入到文档中。默认值是true 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setColumn(int value) {#setColumn-int-}
```
public void setColumn(int value)
```


指定数据源中包含当前记录的唯一数据的列。默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setHash(int value) {#setHash-int-}
```
public void setHash(int value)
```


表示此记录的哈希码。有时 Microsoft Word 使用[getHash()](../../com.aspose.words/odsorecipientdata\#getHash--) / [setHash(int)](../../com.aspose.words/odsorecipientdata\#setHash-int-)整条记录而不是[getUniqueTag()](../../com.aspose.words/odsorecipientdata\#getUniqueTag--) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata\#setUniqueTag-byte---)价值。默认值为 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setUniqueTag(byte[] value) {#setUniqueTag-byte---}
```
public void setUniqueTag(byte[] value)
```


指定包含唯一数据的列中给定记录的内容。默认值为 null 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | byte[] | 对应的字节[] 价值。 |

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
