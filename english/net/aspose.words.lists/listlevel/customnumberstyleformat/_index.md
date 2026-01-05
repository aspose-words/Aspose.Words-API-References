---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: Aspose.Words for .NET
description: Customize your list levels with the ListLevel CustomNumberStyleFormat property. Easily set unique number formats for enhanced document styling.
type: docs
weight: 20
url: /net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Gets or sets the custom number style format for this list level. For example: "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; set; }
```

## Examples

Shows how to get the format for a list with the custom number style.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.That(customNumberStyleFormat, Is.EqualTo("001, 002, 003, ..."));

// We can get value for the specified index of the list item.
Assert.That(ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null), Is.EqualTo("iv"));
Assert.That(ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat), Is.EqualTo("005"));
```

Shows how to set customer number style format.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

doc.UpdateListLabels();

ParagraphCollection paras = doc.FirstSection.Body.Paragraphs;
Assert.That(paras[0].ListLabel.LabelString, Is.EqualTo("001."));
Assert.That(paras[1].ListLabel.LabelString, Is.EqualTo("0001."));
Assert.That(paras[2].ListLabel.LabelString, Is.EqualTo("0002."));

paras[1].ListFormat.ListLevel.CustomNumberStyleFormat = "001, 002, 003, ...";

doc.UpdateListLabels();

Assert.That(paras[0].ListLabel.LabelString, Is.EqualTo("001."));
Assert.That(paras[1].ListLabel.LabelString, Is.EqualTo("001."));
Assert.That(paras[2].ListLabel.LabelString, Is.EqualTo("002."));
```

### See Also

* class [ListLevel](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)
