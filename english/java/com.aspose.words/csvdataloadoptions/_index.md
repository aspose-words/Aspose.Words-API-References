---
title: CsvDataLoadOptions
second_title: Aspose.Words for Java API 参考
description: 表示用于解析 CSV 数据的选项。
type: docs
weight: 98
url: /zh/java/com.aspose.words/csvdataloadoptions/
---

**遗产:**
java.lang.Object
```
public class CsvDataLoadOptions
```

表示用于解析 CSV 数据的选项。

要了解更多信息，请访问**LINQ Reporting Engine**文档文章。

此类的实例可以传递给[CsvDataSource](../../com.aspose.words/csvdatasource).
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [CsvDataLoadOptions()](#CsvDataLoadOptions--) | 使用默认选项初始化此类的新实例。 |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean-) | 通过指定 CSV 数据是否在第一行包含列名来初始化此类的新实例。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getCommentChar()](#getCommentChar--) | 获取用于注释 CSV 数据行的字符。 |
| [getDelimiter()](#getDelimiter--) | 获取要用作列分隔符的字符。 |
| [getQuoteChar()](#getQuoteChar--) | 获取用于引用字段值的字符。 |
| [hasHeaders()](#hasHeaders--) | 获取一个值，该值指示 CSV 数据的第一条记录是否包含列名。 |
| [hasHeaders(boolean value)](#hasHeaders-boolean-) | 设置一个值，该值指示 CSV 数据的第一条记录是否包含列名。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCommentChar(char value)](#setCommentChar-char-) | 设置用于注释 CSV 数据行的字符。 |
| [setDelimiter(char value)](#setDelimiter-char-) | 设置要用作列分隔符的字符。 |
| [setQuoteChar(char value)](#setQuoteChar-char-) | 设置用于引用字段值的字符。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CsvDataLoadOptions() {#CsvDataLoadOptions--}
```
public CsvDataLoadOptions()
```


使用默认选项初始化此类的新实例。

### CsvDataLoadOptions(boolean hasHeaders) {#CsvDataLoadOptions-boolean-}
```
public CsvDataLoadOptions(boolean hasHeaders)
```


通过指定 CSV 数据是否在第一行包含列名来初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| hasHeaders | boolean |  |

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
### getCommentChar() {#getCommentChar--}
```
public char getCommentChar()
```


获取用于注释 CSV 数据行的字符。默认值为'\#'（数字符号）。

**退货:**
char - 用于注释 CSV 数据行的字符。
### getDelimiter() {#getDelimiter--}
```
public char getDelimiter()
```


获取要用作列分隔符的字符。默认值为“,”（逗号）。

**退货:**
char - 用作列分隔符的字符。
### getQuoteChar() {#getQuoteChar--}
```
public char getQuoteChar()
```


获取用于引用字段值的字符。

默认值为 '"'（引号）。

将字符加倍以将其放入引用的文本中。

**退货:**
char - 用于引用字段值的字符。
### hasHeaders() {#hasHeaders--}
```
public boolean hasHeaders()
```


获取一个值，该值指示 CSV 数据的第一条记录是否包含列名。默认值为**false**.

**退货:**
boolean - 一个值，指示 CSV 数据的第一条记录是否包含列名。
### hasHeaders(boolean value) {#hasHeaders-boolean-}
```
public void hasHeaders(boolean value)
```


设置一个值，该值指示 CSV 数据的第一条记录是否包含列名。默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指示 CSV 数据的第一条记录是否包含列名。 |

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




### setCommentChar(char value) {#setCommentChar-char-}
```
public void setCommentChar(char value)
```


设置用于注释 CSV 数据行的字符。默认值为'\#'（数字符号）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | char | 用于注释 CSV 数据行的字符。 |

### setDelimiter(char value) {#setDelimiter-char-}
```
public void setDelimiter(char value)
```


设置要用作列分隔符的字符。默认值为“,”（逗号）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | char | 用作列分隔符的字符。 |

### setQuoteChar(char value) {#setQuoteChar-char-}
```
public void setQuoteChar(char value)
```


设置用于引用字段值的字符。

默认值为 '"'（引号）。

将字符加倍以将其放入引用的文本中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | char | 用于引用字段值的字符。 |

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
