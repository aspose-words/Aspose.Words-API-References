---
title: RevisionTextEffect
second_title: Aspose.Words for Java API 参考
description: 允许为文档文本的修订指定装饰效果。
type: docs
weight: 489
url: /zh/java/com.aspose.words/revisiontexteffect/
---

**遗产:**
java.lang.Object
```
public class RevisionTextEffect
```

允许为文档文本的修订指定装饰效果。
## 字段

| 字段 | 描述 |
| --- | --- |
| [BOLD](#BOLD) | 修改后的内容以粗体和彩色显示。 |
| [COLOR](#COLOR) | 修改后的内容仅用颜色突出显示。 |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | 修改后的内容是双划线和彩色的。 |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | 修改后的内容带有双下划线和彩色。 |
| [HIDDEN](#HIDDEN) | 修改后的内容被隐藏。 |
| [ITALIC](#ITALIC) | 修改后的内容用斜体和彩色显示。 |
| [NONE](#NONE) | 修改后的内容没有应用特殊效果。 |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | 修改后的内容被描边并着色。 |
| [UNDERLINE](#UNDERLINE) | 修改后的内容带有下划线和彩色。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int revisionTextEffect)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int revisionTextEffect)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


修改后的内容以粗体和彩色显示。

### COLOR {#COLOR}
```
public static int COLOR
```


修改后的内容仅用颜色突出显示。

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


修改后的内容是双划线和彩色的。仅适用于[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION), [Revision类型.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE)和[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING)（'移动'类型）。

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


修改后的内容带有双下划线和彩色。

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


修改后的内容被隐藏。仅适用于[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION)和[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING)（'移动'类型）。

### ITALIC {#ITALIC}
```
public static int ITALIC
```


修改后的内容用斜体和彩色显示。

### NONE {#NONE}
```
public static int NONE
```


修改后的内容没有应用特殊效果。这对应于[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


修改后的内容被描边并着色。

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


修改后的内容带有下划线和彩色。

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
### fromName(String revisionTextEffectName) {#fromName-java.lang.String-}
```
public static int fromName(String revisionTextEffectName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int revisionTextEffect) {#getName-int-}
```
public static String getName(int revisionTextEffect)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| revisionTextEffect | int |  |

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
### toString(int revisionTextEffect) {#toString-int-}
```
public static String toString(int revisionTextEffect)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| revisionTextEffect | int |  |

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
