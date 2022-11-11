---
title: WriteProtection
second_title: Aspose.Words for Java API 参考
description:指定文档的写保护设置。
type: docs
weight: 623
url: /zh/java/com.aspose.words/writeprotection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable
```
public class WriteProtection implements Cloneable
```

指定文档的写保护设置。

要了解更多信息，请访问**Protect or Encrypt a Document**文档文章。

写保护指定作者是否建议以只读方式打开文档和/或需要密码才能修改文档。

写保护不同于文档保护。在 Microsoft Word 中的“另存为”对话框的选项中指定写保护。

您不直接创建此类的实例。您可以通过[Document.getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--)财产。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getReadOnlyRecommended()](#getReadOnlyRecommended--) | 指定文档作者是否建议以只读方式打开文档。 |
| [hashCode()](#hashCode--) |  |
| [isWriteProtected()](#isWriteProtected--) | 设置写保护密码时返回 true。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setPassword(String password)](#setPassword-java.lang.String-) | 设置文档的写保护密码。 |
| [setReadOnlyRecommended(boolean value)](#setReadOnlyRecommended-boolean-) | 指定文档作者是否建议以只读方式打开文档。 |
| [toString()](#toString--) |  |
| [validatePassword(String password)](#validatePassword-java.lang.String-) | 如果指定的密码与保护文档的写保护密码相同，则返回 true。 |
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
### getReadOnlyRecommended() {#getReadOnlyRecommended--}
```
public boolean getReadOnlyRecommended()
```


指定文档作者是否建议以只读方式打开文档。

**退货:**
boolean - 对应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isWriteProtected() {#isWriteProtected--}
```
public boolean isWriteProtected()
```


设置写保护密码时返回 true。

**退货:**
boolean - 设置写保护密码时为真。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setPassword(String password) {#setPassword-java.lang.String-}
```
public void setPassword(String password)
```


设置文档的写保护密码。

如果设置了密码，Microsoft Word 将要求用户输入密码或以只读方式打开文档。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| password | java.lang.String | 要设置的密码。不能为空，但可以是空字符串。 |

### setReadOnlyRecommended(boolean value) {#setReadOnlyRecommended-boolean-}
```
public void setReadOnlyRecommended(boolean value)
```


指定文档作者是否建议以只读方式打开文档。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### validatePassword(String password) {#validatePassword-java.lang.String-}
```
public boolean validatePassword(String password)
```


如果指定的密码与保护文档的写保护密码相同，则返回 true。如果文档未使用密码进行写保护，则返回 false。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| password | java.lang.String |  |

**退货:**
布尔值
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
