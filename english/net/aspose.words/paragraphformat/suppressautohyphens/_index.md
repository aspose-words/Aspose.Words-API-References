---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words for .NET
description: Control hyphenation in your document with the ParagraphFormat SuppressAutoHyphens property, ensuring clear and professional paragraph formatting.
type: docs
weight: 380
url: /net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Examples

Shows how to suppress hyphenation for a paragraph.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.That(Hyphenation.IsDictionaryRegistered("de-CH"), Is.True);

// Open a document containing text with a locale matching that of our dictionary.
// When we save this document to a fixed page save format, its text will have hyphenation.
Document doc = new Document(MyDir + "German text.docx");

// We can set the "SuppressAutoHyphens" property to "true" to disable hyphenation
// for a specific paragraph while keeping it enabled for the rest of the document.
// The default value for this property is "false",
// which means every paragraph by default uses hyphenation if any is available.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
