---
title: Create a DOC File Using Aspose.Words for .NET
type: docs
weight: 10
url: /examples/net/create_a_doc_file_using_aspose.words_for.net/
description: "The code snippet explains how to create an Doc file using Aspose.Words for .NET. Classes used for creating document are Document and DocumentBuilder"
---

The following code snippet explains how to create an Doc file using Aspose.Words for .NET. 

1. Create an instance of [Document](../net/aspose.words/document/) class.
2. Intialize [DocumentBuilder](../net/aspose.words/documentbuilder/) with [Document](../net/aspose.words/document/) object.
3. Write your content with [DocumentBuilder.Writeln](../net/aspose.words/documentbuilder/writeln/#writeln_1) method.
4. Save your document with [Document.Save](../net/aspose.words/document/save/#save_2) method.
   
```csharp
// create a blank document
Document doc = new Document();
// the DocumentBuilder class provides members to easily add content to a document
DocumentBuilder builder = new DocumentBuilder(doc);
// write a new paragraph in the document with the text "Hello World!"
builder.Writeln("Hello World!");
// save the document in DOCX format. 
// the format to save as is inferred from the extension of the file name.
doc.Save(dir + "output.docx");
```

### See Also

* class [DocumentBase](../net/aspose.words/documentbase)
* namespace [Aspose.Words](../net/aspose.words)