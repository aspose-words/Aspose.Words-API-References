---
title: SdtListItem
second_title: Aspose.Words for Java API Reference
description: 此元素指定父或结构化文档标记中的单个列表项。
type: docs
weight: 506
url: /zh/java/com.aspose.words/sdtlistitem/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class SdtListItem implements Cloneable
```

此元素指定父项中的单个列表项[Sdt类型.COMBO\_BOX](../../com.aspose.words/sdttype\#COMBO-BOX)或者[Sdt类型.DROP\_DOWN\_LIST](../../com.aspose.words/sdttype\#DROP-DOWN-LIST)结构化文档标签。

要了解更多信息，请访问**Structured Document Tags or Content Control**文档文章。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [SdtListItem(String displayText, String value)](#SdtListItem-java.lang.String-java.lang.String-) | 初始化此类的新实例。 |
| [SdtListItem(String value)](#SdtListItem-java.lang.String-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDisplayText()](#getDisplayText--) | 获取要在运行内容中显示的文本以代替[getValue()](../../com.aspose.words/sdtlistitem\#getValue--)此列表项的属性内容。 |
| [getValue()](#getValue--) | 获取此列表项的值。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### SdtListItem(String displayText, String value) {#SdtListItem-java.lang.String-java.lang.String-}
```
public SdtListItem(String displayText, String value)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| displayText | java.lang.String |  |
| value | java.lang.String |  |

### SdtListItem(String value) {#SdtListItem-java.lang.String-}
```
public SdtListItem(String value)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String |  |

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
### getDisplayText() {#getDisplayText--}
```
public String getDisplayText()
```


获取要在运行内容中显示的文本以代替[getValue()](../../com.aspose.words/sdtlistitem\#getValue--)此列表项的属性内容。

不能为 null，也不能为空字符串。

**退货:**
 java.lang.String - 在运行内容中显示的文本以代替[getValue()](../../com.aspose.words/sdtlistitem\#getValue--)此列表项的属性内容。
### getValue() {#getValue--}
```
public String getValue()
```


获取此列表项的值。

不能为 null，也不能为空字符串。

**退货:**
java.lang.String - 此列表项的值。
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
