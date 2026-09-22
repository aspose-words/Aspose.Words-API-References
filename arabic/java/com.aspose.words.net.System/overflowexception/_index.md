---
title: "OverflowException"
linktitle: "OverflowException"
second_title: "Aspose.Words لـ Java"
description: "الاستثناء الذي يُرمى عندما ينتج عن عملية تحويل أو تحويل حسابية في سياق مُتحقق تجاوز سعة في Java."
type: docs
weight: 10
url: /ar/java/com.aspose.words.net.system/overflowexception/
---

**Inheritance:**
java.lang.Object, java.lang.Throwable, java.lang.Exception, java.lang.RuntimeException, java.lang.ArithmeticException
```
public class OverflowException extends ArithmeticException
```

الاستثناء الذي يُرمى عندما ينتج عن عملية حسابية أو تحويل أو تحويل في سياق مُفحص تجاوزًا للحد الأقصى.
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [OverflowException()](#OverflowException) | ينشئ مثيلًا جديدًا من الفئة [OverflowException](../../com.aspose.words.net.system/overflowexception/). |
| [OverflowException(String message)](#OverflowException-java.lang.String) | ينشئ مثيلًا جديدًا من الفئة [OverflowException](../../com.aspose.words.net.system/overflowexception/) مع رسالة خطأ محددة. |
| [OverflowException(String message, Throwable cause)](#OverflowException-java.lang.String-java.lang.Throwable) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [addSuppressed(Throwable arg0)](#addSuppressed-java.lang.Throwable) |  |
| [fillInStackTrace()](#fillInStackTrace) |  |
| [getCause()](#getCause) |  |
| [getLocalizedMessage()](#getLocalizedMessage) |  |
| [getMessage()](#getMessage) |  |
| [getStackTrace()](#getStackTrace) |  |
| [getSuppressed()](#getSuppressed) |  |
| [initCause(Throwable arg0)](#initCause-java.lang.Throwable) |  |
| [printStackTrace()](#printStackTrace) |  |
| [printStackTrace(PrintStream arg0)](#printStackTrace-java.io.PrintStream) |  |
| [printStackTrace(PrintWriter arg0)](#printStackTrace-java.io.PrintWriter) |  |
| [setStackTrace(StackTraceElement[] arg0)](#setStackTrace-java.lang.StackTraceElement) |  |
| [toString()](#toString) |  |
### OverflowException() {#OverflowException}
```
public OverflowException()
```


ينشئ مثيلًا جديدًا من الفئة [OverflowException](../../com.aspose.words.net.system/overflowexception/).

### OverflowException(String message) {#OverflowException-java.lang.String}
```
public OverflowException(String message)
```


ينشئ مثيلًا جديدًا من الفئة [OverflowException](../../com.aspose.words.net.system/overflowexception/) مع رسالة خطأ محددة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| message | java.lang.String | الرسالة التي تصف الخطأ. |

### OverflowException(String message, Throwable cause) {#OverflowException-java.lang.String-java.lang.Throwable}
```
public OverflowException(String message, Throwable cause)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| message | java.lang.String |  |
| cause | java.lang.Throwable |  |

### addSuppressed(Throwable arg0) {#addSuppressed-java.lang.Throwable}
```
public final synchronized void addSuppressed(Throwable arg0)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| arg0 | java.lang.Throwable |  |

### fillInStackTrace() {#fillInStackTrace}
```
public synchronized Throwable fillInStackTrace()
```




**Returns:**
java.lang.Throwable
### getCause() {#getCause}
```
public synchronized Throwable getCause()
```




**Returns:**
java.lang.Throwable
### getLocalizedMessage() {#getLocalizedMessage}
```
public String getLocalizedMessage()
```




**Returns:**
java.lang.String
### getMessage() {#getMessage}
```
public String getMessage()
```




**Returns:**
java.lang.String
### getStackTrace() {#getStackTrace}
```
public StackTraceElement[] getStackTrace()
```




**Returns:**
java.lang.StackTraceElement[]
### getSuppressed() {#getSuppressed}
```
public final synchronized Throwable[] getSuppressed()
```




**Returns:**
java.lang.Throwable[]
### initCause(Throwable arg0) {#initCause-java.lang.Throwable}
```
public synchronized Throwable initCause(Throwable arg0)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| arg0 | java.lang.Throwable |  |

**Returns:**
java.lang.Throwable
### printStackTrace() {#printStackTrace}
```
public void printStackTrace()
```




### printStackTrace(PrintStream arg0) {#printStackTrace-java.io.PrintStream}
```
public void printStackTrace(PrintStream arg0)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| arg0 | java.io.PrintStream |  |

### printStackTrace(PrintWriter arg0) {#printStackTrace-java.io.PrintWriter}
```
public void printStackTrace(PrintWriter arg0)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| arg0 | java.io.PrintWriter |  |

### setStackTrace(StackTraceElement[] arg0) {#setStackTrace-java.lang.StackTraceElement}
```
public void setStackTrace(StackTraceElement[] arg0)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| arg0 | java.lang.StackTraceElement[] |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
