---
title: IFieldResultFormatter
second_title: Aspose.Words for Java API 参考
description: 如果您想控制字段结果的格式，请实现此接口。
type: docs
weight: 642
url: /zh/java/com.aspose.words/ifieldresultformatter/
---
```
public interface IFieldResultFormatter
```

如果您想控制字段结果的格式，请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [format(double value, int format)](#format-double-int-) |  |
| [format(String value, int format)](#format-java.lang.String-int-) |  |
| [formatDateTime(Date value, String format, int calendarType)](#formatDateTime-java.util.Date-java.lang.String-int-) |  |
| [formatNumeric(double value, String format)](#formatNumeric-double-java.lang.String-) | 当 Aspose.Words 应用数字格式开关时调用，即 |
### format(double value, int format) {#format-double-int-}
```
public abstract String format(double value, int format)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |
| format | int |  |

**退货：**
java.lang.字符串
### format(String value, int format) {#format-java.lang.String-int-}
```
public abstract String format(String value, int format)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String |  |
| format | int |  |

**退货：**
java.lang.字符串
### formatDateTime(Date value, String format, int calendarType) {#formatDateTime-java.util.Date-java.lang.String-int-}
```
public abstract String formatDateTime(Date value, String format, int calendarType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date |  |
| format | java.lang.String |  |
| calendarType | int |  |

**退货：**
java.lang.字符串
### formatNumeric(double value, String format) {#formatNumeric-double-java.lang.String-}
```
public abstract String formatNumeric(double value, String format)
```


当 Aspose.Words 应用数字格式开关时调用，即\\\#”\#。\ #”。执行应该返回**null**指示应应用默认格式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |
| format | java.lang.String |  |

**退货：**
java.lang.字符串