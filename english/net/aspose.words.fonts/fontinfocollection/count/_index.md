---
title: FontInfoCollection.Count
second_title: Aspose.Words for .NET API Reference
description: FontInfoCollection property. Gets the number of elements contained in the collection in C#.
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
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### See Also

* class [FontInfoCollection](../)
* namespace [Aspose.Words.Fonts](../../fontinfocollection/)
* assembly [Aspose.Words](../../../)
