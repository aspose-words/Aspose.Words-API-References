---
title: CompareOptions
second_title: Aspose.Words for Java API 参考
description: 允许选择文档比较操作的高级选项。
type: docs
weight: 81
url: /zh/java/com.aspose.words/compareoptions/
---

**遗产:**
java.lang.Object
```
public class CompareOptions
```

允许选择文档比较操作的高级选项。

要了解更多信息，请访问**Compare Documents**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getGranularity()](#getGranularity--) | 指定是按字符还是按单词跟踪更改。 |
| [getIgnoreCaseChanges()](#getIgnoreCaseChanges--) | True 表示文档比较不区分大小写。 |
| [getIgnoreComments()](#getIgnoreComments--) | 指定是否比较注释中的差异。 |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId--) | 指定是否忽略 DrawingML 唯一 ID 中的差异。 |
| [getIgnore字段()](#getIgnore字段--) | 指定是否比较字段的差异。 |
| [getIgnoreFootnotes()](#getIgnoreFootnotes--) | 指定是否比较脚注和尾注的差异。 |
| [getIgnoreFormatting()](#getIgnoreFormatting--) | True 表示忽略格式。 |
| [getIgnoreHeadersAndFooters()](#getIgnoreHeadersAndFooters--) | True 表示忽略页眉和页脚内容。 |
| [getIgnoreTables()](#getIgnoreTables--) | 指定是否比较表中包含的数据的差异。 |
| [getIgnoreTextboxes()](#getIgnoreTextboxes--) | 指定是否比较文本框中包含的数据的差异。 |
| [getTarget()](#getTarget--) | 指定在比较期间应将哪个文档用作目标。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setGranularity(int value)](#setGranularity-int-) | 指定是按字符还是按单词跟踪更改。 |
| [setIgnoreCaseChanges(boolean value)](#setIgnoreCaseChanges-boolean-) | True 表示文档比较不区分大小写。 |
| [setIgnoreComments(boolean value)](#setIgnoreComments-boolean-) | 指定是否比较注释中的差异。 |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean-) | 指定是否忽略 DrawingML 唯一 ID 中的差异。 |
| [setIgnore字段(boolean value)](#setIgnore字段-boolean-) | 指定是否比较字段的差异。 |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean-) | 指定是否比较脚注和尾注的差异。 |
| [setIgnoreFormatting(boolean value)](#setIgnoreFormatting-boolean-) | True 表示忽略格式。 |
| [setIgnoreHeadersAndFooters(boolean value)](#setIgnoreHeadersAndFooters-boolean-) | True 表示忽略页眉和页脚内容。 |
| [setIgnoreTables(boolean value)](#setIgnoreTables-boolean-) | 指定是否比较表中包含的数据的差异。 |
| [setIgnoreTextboxes(boolean value)](#setIgnoreTextboxes-boolean-) | 指定是否比较文本框中包含的数据的差异。 |
| [setTarget(int value)](#setTarget-int-) | 指定在比较期间应将哪个文档用作目标。 |
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
### getGranularity() {#getGranularity--}
```
public int getGranularity()
```


指定是按字符还是按单词跟踪更改。默认值为[Granularity.WORD\_LEVEL](../../com.aspose.words/granularity\#WORD-LEVEL).

**退货:**
int - 对应的 int 值。返回值是以下之一[Granularity](../../com.aspose.words/granularity)常数。
### getIgnoreCaseChanges() {#getIgnoreCaseChanges--}
```
public boolean getIgnoreCaseChanges()
```


True 表示文档比较不区分大小写。默认情况下，比较区分大小写。

**退货:**
boolean - 对应的布尔值。
### getIgnoreComments() {#getIgnoreComments--}
```
public boolean getIgnoreComments()
```


指定是否比较注释中的差异。默认情况下不会忽略注释。

**退货:**
boolean - 对应的布尔值。
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId--}
```
public boolean getIgnoreDmlUniqueId()
```


指定是否忽略 DrawingML 唯一 ID 中的差异。默认值为**false**.

**退货:**
boolean - 对应的布尔值。
### getIgnore字段() {#getIgnore字段--}
```
public boolean getIgnore字段()
```


指定是否比较字段的差异。默认情况下，不会忽略字段。

**退货:**
boolean - 对应的布尔值。
### getIgnoreFootnotes() {#getIgnoreFootnotes--}
```
public boolean getIgnoreFootnotes()
```


指定是否比较脚注和尾注的差异。默认情况下不会忽略脚注。

**退货:**
boolean - 对应的布尔值。
### getIgnoreFormatting() {#getIgnoreFormatting--}
```
public boolean getIgnoreFormatting()
```


True 表示忽略格式。默认情况下，不会忽略文档格式。

**退货:**
boolean - 对应的布尔值。
### getIgnoreHeadersAndFooters() {#getIgnoreHeadersAndFooters--}
```
public boolean getIgnoreHeadersAndFooters()
```


True 表示忽略页眉和页脚内容。默认情况下，不会忽略页眉和页脚。

**退货:**
boolean - 对应的布尔值。
### getIgnoreTables() {#getIgnoreTables--}
```
public boolean getIgnoreTables()
```


指定是否比较表中包含的数据的差异。默认情况下，不会忽略表。

**退货:**
boolean - 对应的布尔值。
### getIgnoreTextboxes() {#getIgnoreTextboxes--}
```
public boolean getIgnoreTextboxes()
```


指定是否比较文本框中包含的数据的差异。默认情况下，文本框不会被忽略。

**退货:**
boolean - 对应的布尔值。
### getTarget() {#getTarget--}
```
public int getTarget()
```


指定在比较期间应将哪个文档用作目标。

**退货:**
int - 对应的 int 值。返回值是以下之一[ComparisonTarget类型](../../com.aspose.words/comparisontargettype)常数。
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




### setGranularity(int value) {#setGranularity-int-}
```
public void setGranularity(int value)
```


指定是按字符还是按单词跟踪更改。默认值为[Granularity.WORD\_LEVEL](../../com.aspose.words/granularity\#WORD-LEVEL).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[Granularity](../../com.aspose.words/granularity)常数。 |

### setIgnoreCaseChanges(boolean value) {#setIgnoreCaseChanges-boolean-}
```
public void setIgnoreCaseChanges(boolean value)
```


True 表示文档比较不区分大小写。默认情况下，比较区分大小写。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnoreComments(boolean value) {#setIgnoreComments-boolean-}
```
public void setIgnoreComments(boolean value)
```


指定是否比较注释中的差异。默认情况下不会忽略注释。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean-}
```
public void setIgnoreDmlUniqueId(boolean value)
```


指定是否忽略 DrawingML 唯一 ID 中的差异。默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnore字段(boolean value) {#setIgnore字段-boolean-}
```
public void setIgnore字段(boolean value)
```


指定是否比较字段的差异。默认情况下，不会忽略字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean-}
```
public void setIgnoreFootnotes(boolean value)
```


指定是否比较脚注和尾注的差异。默认情况下不会忽略脚注。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnoreFormatting(boolean value) {#setIgnoreFormatting-boolean-}
```
public void setIgnoreFormatting(boolean value)
```


True 表示忽略格式。默认情况下，不会忽略文档格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnoreHeadersAndFooters(boolean value) {#setIgnoreHeadersAndFooters-boolean-}
```
public void setIgnoreHeadersAndFooters(boolean value)
```


True 表示忽略页眉和页脚内容。默认情况下，不会忽略页眉和页脚。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnoreTables(boolean value) {#setIgnoreTables-boolean-}
```
public void setIgnoreTables(boolean value)
```


指定是否比较表中包含的数据的差异。默认情况下，不会忽略表。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnoreTextboxes(boolean value) {#setIgnoreTextboxes-boolean-}
```
public void setIgnoreTextboxes(boolean value)
```


指定是否比较文本框中包含的数据的差异。默认情况下，文本框不会被忽略。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setTarget(int value) {#setTarget-int-}
```
public void setTarget(int value)
```


指定在比较期间应将哪个文档用作目标。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[ComparisonTarget类型](../../com.aspose.words/comparisontargettype)常数。 |

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
