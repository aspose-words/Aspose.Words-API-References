---
title: DocSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words for .NET
description: DocSaveOptions Password property. Gets/sets a password to encrypt document using RC4 encryption method in C#.
type: docs
weight: 30
url: /net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

Gets/sets a password to encrypt document using RC4 encryption method.

```csharp
public string Password { get; set; }
```

## Remarks

In order to save document without encryption this property should be `null` or empty string.

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

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### See Also

* class [DocSaveOptions](../)
* namespace [Aspose.Words.Saving](../../docsaveoptions/)
* assembly [Aspose.Words](../../../)
