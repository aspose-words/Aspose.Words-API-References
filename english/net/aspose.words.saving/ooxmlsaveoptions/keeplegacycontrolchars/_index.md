---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: Aspose.Words for .NET
description: Discover OoxmlSaveOptions' KeepLegacyControlChars property to maintain the original format of legacy control characters for seamless document conversion.
type: docs
weight: 50
url: /net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

Keeps original representation of legacy control characters.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

## Examples

Shows how to support legacy control characters when converting to .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "KeepLegacyControlChars" property to "true" to preserve
// the "ShortDateTime" legacy character while saving.
// Set the "KeepLegacyControlChars" property to "false" to remove
// the "ShortDateTime" legacy character from the output document.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.That(doc.FirstSection.Body.GetText(), Is.EqualTo(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f"));
```

### See Also

* class [OoxmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
