---
title: SaveOutputParameters
linktitle: SaveOutputParameters
second_title: Aspose.Words for Java
description: This object is returned to the caller after a document is saved and contains additional information that has been generated or calculated during the save operation in Java.
type: docs
weight: 521
url: /java/com.aspose.words/saveoutputparameters/
---

**Inheritance:**
java.lang.Object
```
public class SaveOutputParameters
```

This object is returned to the caller after a document is saved and contains additional information that has been generated or calculated during the save operation. The caller can use or ignore this object.

To learn more, visit the [ Save a Document ][Save a Document] documentation article.

 **Examples:** 

Shows how to access output parameters of a document's save operation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
 SaveOutputParameters parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.doc");

 Assert.assertEquals("application/msword", parameters.getContentType());

 // This property changes depending on the save format.
 parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.pdf");

 Assert.assertEquals("application/pdf", parameters.getContentType());
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getContentType()](#getContentType) | Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getContentType() {#getContentType}
```
public String getContentType()
```


Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document.

 **Examples:** 

Shows how to access output parameters of a document's save operation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
 SaveOutputParameters parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.doc");

 Assert.assertEquals("application/msword", parameters.getContentType());

 // This property changes depending on the save format.
 parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.pdf");

 Assert.assertEquals("application/pdf", parameters.getContentType());
 
```

**Returns:**
java.lang.String - The Content-Type string (Internet Media Type) that identifies the type of the saved document.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

