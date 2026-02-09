---
title: IncorrectPasswordException Class
linktitle: IncorrectPasswordException
articleTitle: IncorrectPasswordException
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.IncorrectPasswordException class, which handles password errors for encrypted documents, ensuring secure and seamless access.
type: docs
weight: 3730
url: /net/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException class

Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public class IncorrectPasswordException : Exception
```

## Examples

Shows how to set save options for older Microsoft Word formats.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
// Note that this does not encrypt the contents of the document in any way.
options.Password = "MyPassword";

// If the document contains a routing slip, we can preserve it while saving by setting this flag to true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// To be able to load the document,
// we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello world!"));
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
