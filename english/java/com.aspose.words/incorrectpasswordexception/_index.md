---
title: IncorrectPasswordException
linktitle: IncorrectPasswordException
second_title: Aspose.Words for Java
description: Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing in Java.
type: docs
weight: 393
url: /java/com.aspose.words/incorrectpasswordexception/
---

**Inheritance:**
java.lang.Object, java.lang.Throwable, java.lang.Exception
```
public class IncorrectPasswordException extends Exception
```

Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

 **Examples:** 

Shows how to set save options for older Microsoft Word formats.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Hello world!");

 DocSaveOptions options = new DocSaveOptions(SaveFormat.DOC);

 // Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
 // Note that this does not encrypt the contents of the document in any way.
 options.setPassword("MyPassword");

 // If the document contains a routing slip, we can preserve it while saving by setting this flag to true.
 options.setSaveRoutingSlip(true);

 doc.save(getArtifactsDir() + "DocSaveOptions.SaveAsDoc.doc", options);

 // To be able to load the document,
 // we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
 Assert.assertThrows(IncorrectPasswordException.class, () -> new Document(getArtifactsDir() + "DocSaveOptions.SaveAsDoc.doc"));

 LoadOptions loadOptions = new LoadOptions("MyPassword");
 doc = new Document(getArtifactsDir() + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

 Assert.assertEquals("Hello world!", doc.getText().trim());
 
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
