---
title: SdtCalendar类型
second_title: Aspose.Words for Java API Reference
description: 指定可用于在 Office Open XML 文档中指定 / 的可能类型的日历。
type: docs
weight: 504
url: /zh/java/com.aspose.words/sdtcalendartype/
---

**遗产:**
java.lang.Object
```
public class SdtCalendar类型
```

指定可用于指定的可能的日历类型[StructuredDocumentTag.getCalendar类型()](../../com.aspose.words/structureddocumenttag\#getCalendar类型--) / [StructuredDocumentTag.setCalendar类型(int)](../../com.aspose.words/structureddocumenttag\#setCalendar类型-int-)在 Office Open XML 文档中。
## 字段

| 字段 | 描述 |
| --- | --- |
| [DEFAULT](#DEFAULT) | 在 OOXML 中用作默认值。 |
| [GREGORIAN](#GREGORIAN) | 指定应使用 ISO 8601 中定义的公历。 |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | 指定应使用 ISO 8601 中定义的公历。 |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | 指定应使用 ISO 8601 中定义的公历。 |
| [GREGORIAN_US](#GREGORIAN-US) | 指定应使用 ISO 8601 中定义的公历。 |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | 指定应使用 ISO 8601 中定义的公历。 |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | 指定应使用 ISO 8601 中定义的公历。 |
| [HEBREW](#HEBREW) | 指定希伯来农历，如逾越节的高斯公式所述[引文]和口述法的完整重述（Mishneh Torah），应使用。 |
| [HIJRI](#HIJRI) | 指定回历农历，如沙特阿拉伯王国伊斯兰事务部、捐赠基金、Da\\u2018wah 和指导，应使用。 |
| [JAPAN](#JAPAN) | 指定应使用日本工业标准 JIS X 0301 所描述的日本天皇时代日历。 |
| [KOREA](#KOREA) | 指定韩国檀君时代的历法，如韩国法律颁布第 1 号所述。 |
| [NONE](#NONE) | 指定不应使用日历。 |
| [SAKA](#SAKA) | 指定应使用印度历法改革委员会所描述的萨卡时代历法，作为印度星历和航海年历的一部分。 |
| [TAIWAN](#TAIWAN) | 指定应使用由中国国家标准 CNS 7648 定义的台湾日历。 |
| [THAI](#THAI) | 指定由 HM 皇家法令定义的泰国日历 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String sdtCalendar类型Name)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int sdtCalendar类型)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int sdtCalendar类型)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


在 OOXML 中用作默认值。等于[GREGORIAN](../../com.aspose.words/sdtcalendartype\#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


指定应使用 ISO 8601 中定义的公历。此日历应本地化为适当的语言。

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


指定应使用 ISO 8601 中定义的公历。此日历的值应以阿拉伯语显示。

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


指定应使用 ISO 8601 中定义的公历。此日历的值应以中东法语显示。

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


指定应使用 ISO 8601 中定义的公历。此日历的值应以英文显示。

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


指定应使用 ISO 8601 中定义的公历。此日历的值应该是对应阿拉伯字符中英文字符串的表示（格里高利历中英文的阿拉伯音译）。

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


指定应使用 ISO 8601 中定义的公历。此日历的值应该是对应阿拉伯字符中法语字符串的表示（公历中法语的阿拉伯语音译）。

### HEBREW {#HEBREW}
```
public static int HEBREW
```


指定希伯来农历，如逾越节的高斯公式所述[引文]和口述法的完整重述（Mishneh Torah），应使用。

### HIJRI {#HIJRI}
```
public static int HIJRI
```


指定回历农历，如沙特阿拉伯王国伊斯兰事务部、捐赠基金、Da\\u2018wah 和指导，应使用。

### JAPAN {#JAPAN}
```
public static int JAPAN
```


指定应使用日本工业标准 JIS X 0301 所描述的日本天皇时代日历。

### KOREA {#KOREA}
```
public static int KOREA
```


指定应使用韩国法律第 4 号所述的韩国檀君时代日历。

### NONE {#NONE}
```
public static int NONE
```


指定不应使用日历。通常在 AW 中，None 是枚举的第一个默认值，但在这种情况下不是。 None 不是 OOXML 的默认值，而是[GREGORIAN](../../com.aspose.words/sdtcalendartype\#GREGORIAN)是默认值，并且是此枚举的第一个成员。

### SAKA {#SAKA}
```
public static int SAKA
```


指定应使用印度历法改革委员会所描述的萨卡时代历法，作为印度星历和航海年历的一部分。

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


指定应使用由中国国家标准 CNS 7648 定义的台湾日历。

### THAI {#THAI}
```
public static int THAI
```


指定泰国历法，如皇家公报 BE 2456（公元 1913 年）中的 HM King Vajiravudh（拉玛六世）的皇家法令和总理披汶颂喀拉姆（公元 1941 年）的法令所定义的，以公历 1 月 1 日开始这一年并将零年映射到公历 543 BC，应使用。

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
### fromName(String sdtCalendar类型Name) {#fromName-java.lang.String-}
```
public static int fromName(String sdtCalendar类型Name)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sdtCalendar类型Name | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int sdtCalendar类型) {#getName-int-}
```
public static String getName(int sdtCalendar类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sdtCalendar类型 | int |  |

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
### toString(int sdtCalendar类型) {#toString-int-}
```
public static String toString(int sdtCalendar类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sdtCalendar类型 | int |  |

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
