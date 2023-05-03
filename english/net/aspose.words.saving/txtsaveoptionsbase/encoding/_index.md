---
title: TxtSaveOptionsBase.Encoding
linktitle: Encoding
second_title: Aspose.Words for .NET API Reference
description: TxtSaveOptionsBase Encoding property. Specifies the encoding to use when exporting in text formats. Default value is Encoding.UTF8 in C#.
type: docs
weight: 10
url: /net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## Encoding property

Specifies the encoding to use when exporting in text formats. Default value is **Encoding.UTF8**.

```csharp
public Encoding Encoding { get; set; }
```

## Examples

Shows how to set encoding for a .txt output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add some text with characters from outside the ASCII character set.
builder.Write("À È Ì Ò Ù.");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Verify that the "Encoding" property contains the appropriate encoding for our document's contents.
Assert.AreEqual(System.Text.Encoding.UTF8, txtSaveOptions.Encoding);

doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

string docText = System.Text.Encoding.UTF8.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt"));

Assert.AreEqual("\uFEFFÀ È Ì Ò Ù.\r\n", docText);

// Using an unsuitable encoding may result in a loss of document contents.
txtSaveOptions.Encoding = System.Text.Encoding.ASCII;
doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System.Text.Encoding.ASCII.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt"));

Assert.AreEqual("? ? ? ? ?.\r\n", docText);
```

### See Also

* class [TxtSaveOptionsBase](../)
* namespace [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* assembly [Aspose.Words](../../../)
