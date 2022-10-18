---
title: IFieldResultFormatter
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to control how the field result is formatted.
type: docs
weight: 642
url: /java/com.aspose.words/ifieldresultformatter/
---
```
public interface IFieldResultFormatter
```

Implement this interface if you want to control how the field result is formatted.
## Methods

| Method | Description |
| --- | --- |
| [formatNumeric(double value, String format)](#formatNumeric-double-java.lang.String-) | Called when Aspose.Words applies a numeric format switch, i.e. |
| [formatDateTime(Date value, String format, int calendarType)](#formatDateTime-java.util.Date-java.lang.String-int-) |  |
| [format(String value, int format)](#format-java.lang.String-int-) |  |
| [format(double value, int format)](#format-double-int-) |  |
### formatNumeric(double value, String format) {#formatNumeric-double-java.lang.String-}
```
public abstract String formatNumeric(double value, String format)
```


Called when Aspose.Words applies a numeric format switch, i.e. \\\# "\#.\#". The implementation should return **null** to indicate that the default formatting should be applied.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |
| format | java.lang.String |  |

**Returns:**
java.lang.String
### formatDateTime(Date value, String format, int calendarType) {#formatDateTime-java.util.Date-java.lang.String-int-}
```
public abstract String formatDateTime(Date value, String format, int calendarType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date |  |
| format | java.lang.String |  |
| calendarType | int |  |

**Returns:**
java.lang.String
### format(String value, int format) {#format-java.lang.String-int-}
```
public abstract String format(String value, int format)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String |  |
| format | int |  |

**Returns:**
java.lang.String
### format(double value, int format) {#format-double-int-}
```
public abstract String format(double value, int format)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |
| format | int |  |

**Returns:**
java.lang.String
