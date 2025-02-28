---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words for .NET
description: Secure your documents with OoxmlSaveOptions! Easily set a password for encryption using the ECMA376 Standard for enhanced data protection.
type: docs
weight: 60
url: /net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm.

```csharp
public string Password { get; set; }
```

## Remarks

In order to save document without encryption this property should be `null` or empty string.

## Examples

Shows how to create a password encrypted Office Open XML document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// We will not be able to open this document with Microsoft Word or
// Aspose.Words without providing the correct password.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// Open the encrypted document by passing the correct password in a LoadOptions object.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### See Also

* class [OoxmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
