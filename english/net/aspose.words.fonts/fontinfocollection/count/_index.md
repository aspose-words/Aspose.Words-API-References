---
title: FontInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: Discover the FontInfoCollection Count property, effortlessly retrieve the total number of elements in your collection for seamless data management.
type: docs
weight: 10
url: /net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

Gets the number of elements contained in the collection.

```csharp
public int Count { get; }
```

## Examples

Shows info about the fonts that are present in the blank document.

```csharp
Document doc = new Document();

// A blank document contains 3 default fonts. Each font in the document
// will have a corresponding FontInfo object which contains details about that font.
Assert.That(doc.FontInfos.Count, Is.EqualTo(3));

Assert.That(doc.FontInfos.Contains("Times New Roman"), Is.True);
Assert.That(doc.FontInfos["Times New Roman"].Charset, Is.EqualTo(204));

Assert.That(doc.FontInfos.Contains("Symbol"), Is.True);
Assert.That(doc.FontInfos.Contains("Arial"), Is.True);
```

### See Also

* class [FontInfoCollection](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
