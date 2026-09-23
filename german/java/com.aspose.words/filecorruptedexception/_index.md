---
title: "FileCorruptedException"
linktitle: "FileCorruptedException"
second_title: "Aspose.Words für Java"
description: "Wird beim Laden des Dokuments ausgelöst, wenn das Dokument beschädigt zu sein scheint und in Java nicht geladen werden kann."
type: docs
weight: 307
url: /de/java/com.aspose.words/filecorruptedexception/
---

**Inheritance:**
java.lang.Object, java.lang.Throwable, java.lang.Exception
```
public class FileCorruptedException extends Exception
```

Wird beim Laden des Dokuments ausgelöst, wenn das Dokument beschädigt zu sein scheint und nicht geladen werden kann.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Zeigt, wie man eine FileCorruptedException abfängt.

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
## Methoden

| Methode | Beschreibung |
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
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| arg0 | java.io.PrintStream |  |

### printStackTrace(PrintWriter arg0) {#printStackTrace-java.io.PrintWriter}
```
public void printStackTrace(PrintWriter arg0)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| arg0 | java.io.PrintWriter |  |

### setStackTrace(StackTraceElement[] arg0) {#setStackTrace-java.lang.StackTraceElement}
```
public void setStackTrace(StackTraceElement[] arg0)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| arg0 | java.lang.StackTraceElement[] |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
