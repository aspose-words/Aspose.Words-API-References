---
title: SaveOutputParameters
linktitle: SaveOutputParameters
second_title: Aspose.Words for Java
description: This object is returned to the caller after a document is saved and contains additional information that has been generated or calculated during the save operation in Java.
type: docs
weight: 558
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
| [getContentType()](#getContentType) | Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document. |
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
