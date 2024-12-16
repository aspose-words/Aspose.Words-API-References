---
title: FileCorruptedException
linktitle: FileCorruptedException
second_title: Aspose.Words for Java
description: Thrown during document load when the document appears to be corrupted and impossible to load in Java.
type: docs
weight: 300
url: /java/com.aspose.words/filecorruptedexception/
---

**Inheritance:**
java.lang.Object, java.lang.Throwable, java.lang.Exception
```
public class FileCorruptedException extends Exception
```

Thrown during document load, when the document appears to be corrupted and impossible to load.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

 **Examples:** 

Shows how to catch a FileCorruptedException.

```

 try {
     // If we get an "Unreadable content" error message when trying to open a document using Microsoft Word,
     // chances are that we will get an exception thrown when trying to load that document using Aspose.Words.
     Document doc = new Document(getMyDir() + "Corrupted document.docx");
 } catch (FileCorruptedException e) {
     System.out.println(e.getMessage());
 }
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Methods

| Method | Description |
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
### addSuppressed(Throwable arg0) {#addSuppressed-java.lang.Throwable}
```
public final synchronized void addSuppressed(Throwable arg0)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.io.PrintStream |  |

### printStackTrace(PrintWriter arg0) {#printStackTrace-java.io.PrintWriter}
```
public void printStackTrace(PrintWriter arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.io.PrintWriter |  |

### setStackTrace(StackTraceElement[] arg0) {#setStackTrace-java.lang.StackTraceElement}
```
public void setStackTrace(StackTraceElement[] arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.StackTraceElement[] |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
