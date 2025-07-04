---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words for .NET
description: Discover if FontInfoCollection includes a specific font by name. Easily manage and access your font collection with this essential method.
type: docs
weight: 60
url: /net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Determines whether the collection contains a font with the given name.

```csharp
public bool Contains(string name)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | Case-insensitive name of the font to locate. |

### Return Value

`true` if the item is found in the collection; otherwise, `false`.

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
