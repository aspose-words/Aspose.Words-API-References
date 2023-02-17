---
title: ListLevel.CustomNumberStyleFormat
second_title: Aspose.Words for .NET API Reference
description: ListLevel property. Gets the custom number style format for this list level. For example a ç ĝ  in C#.
type: docs
weight: 20
url: /net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Gets the custom number style format for this list level. For example: "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; }
```

## Examples

Shows how to get the format for a list with the custom number style.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// We can get value for the specified index of the list item.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### See Also

* class [ListLevel](../)
* namespace [Aspose.Words.Lists](../../listlevel/)
* assembly [Aspose.Words](../../../)
