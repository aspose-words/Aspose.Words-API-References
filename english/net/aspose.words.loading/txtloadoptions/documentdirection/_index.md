---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words for .NET
description: Discover the TxtLoadOptions DocumentDirection property to easily set document direction. Optimize your layout with the default LeftToRight setting!
type: docs
weight: 50
url: /net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Gets or sets a document direction. The default value is LeftToRight.

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## Examples

Shows how to detect plaintext document text direction.

```csharp
// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
// the direction of every paragraph of text that Aspose.Words loads from plaintext.
// Each paragraph's "Bidi" property will store its direction.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Detect Hebrew text as right-to-left.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.That(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi, Is.True);

// Detect English text as right-to-left.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.That(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi, Is.False);
```

### See Also

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
