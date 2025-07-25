---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.DocumentDirection enum to easily control text flow in your documents. Enhance readability and formatting with this powerful feature!
type: docs
weight: 4020
url: /net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

Allows to specify the direction to flow the text in a document.

```csharp
public enum DocumentDirection
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| LeftToRight | `0` | Left to right direction. |
| RightToLeft | `1` | Right to left direction. |
| Auto | `2` | Auto-detect direction. |

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

* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
