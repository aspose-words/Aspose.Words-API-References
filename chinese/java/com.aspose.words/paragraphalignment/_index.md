---
title: ParagraphAlignment
second_title: Aspose.Words for Java API 参考
description: 指定段落中的文本对齐方式。
type: docs
weight: 444
url: /zh/java/com.aspose.words/paragraphalignment/
---

**遗产:**
java.lang.Object
```
public class ParagraphAlignment
```

指定段落中的文本对齐方式。
## 字段

| 场地 | 描述 |
| --- | --- |
| [ARABIC_HIGH_KASHIDA](#ARABIC-HIGH-KASHIDA) | 仅限阿拉伯语。 |
| [ARABIC_LOW_KASHIDA](#ARABIC-LOW-KASHIDA) | 仅限阿拉伯语。 |
| [ARABIC_MEDIUM_KASHIDA](#ARABIC-MEDIUM-KASHIDA) | 仅限阿拉伯语。 |
| [CENTER](#CENTER) | 文本水平居中。 |
| [DISTRIBUTED](#DISTRIBUTED) | 文字分布均匀。 |
| [JUSTIFY](#JUSTIFY) | 文本左右对齐。 |
| [LEFT](#LEFT) | 文本左对齐。 |
| [MATH_ELEMENT_CENTER_AS_GROUP](#MATH-ELEMENT-CENTER-AS-GROUP) | 一行中唯一的数学元素，对齐为“居中作为组”。 |
| [RIGHT](#RIGHT) | 文本向右对齐。 |
| [THAI_DISTRIBUTED](#THAI-DISTRIBUTED) | 仅限泰语。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String paragraphAlignmentName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int paragraphAlignment)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int paragraphAlignment)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ARABIC_HIGH_KASHIDA {#ARABIC-HIGH-KASHIDA}
```
public static int ARABIC_HIGH_KASHIDA
```


仅限阿拉伯语。文本的 Kashida 长度已扩展到其可能的最大长度。

### ARABIC_LOW_KASHIDA {#ARABIC-LOW-KASHIDA}
```
public static int ARABIC_LOW_KASHIDA
```


仅限阿拉伯语。文本的 Kashida 长度扩展为稍长的长度。

### ARABIC_MEDIUM_KASHIDA {#ARABIC-MEDIUM-KASHIDA}
```
public static int ARABIC_MEDIUM_KASHIDA
```


仅限阿拉伯语。文本的 Kashida 长度扩展为消费者确定的中等长度。

### CENTER {#CENTER}
```
public static int CENTER
```


文本水平居中。

### DISTRIBUTED {#DISTRIBUTED}
```
public static int DISTRIBUTED
```


文字分布均匀。

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


文本左右对齐。

### LEFT {#LEFT}
```
public static int LEFT
```


文本左对齐。

### MATH_ELEMENT_CENTER_AS_GROUP {#MATH-ELEMENT-CENTER-AS-GROUP}
```
public static int MATH_ELEMENT_CENTER_AS_GROUP
```


一行中唯一的数学元素，对齐为“居中作为组”。

### RIGHT {#RIGHT}
```
public static int RIGHT
```


文本向右对齐。

### THAI_DISTRIBUTED {#THAI-DISTRIBUTED}
```
public static int THAI_DISTRIBUTED
```


仅限泰语。文本通过对泰语的优化来证明是合理的。

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
### fromName(String paragraphAlignmentName) {#fromName-java.lang.String-}
```
public static int fromName(String paragraphAlignmentName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paragraphAlignmentName | java.lang.String |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int paragraphAlignment) {#getName-int-}
```
public static String getName(int paragraphAlignment)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paragraphAlignment | int |  |

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
### toString(int paragraphAlignment) {#toString-int-}
```
public static String toString(int paragraphAlignment)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paragraphAlignment | int |  |

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
