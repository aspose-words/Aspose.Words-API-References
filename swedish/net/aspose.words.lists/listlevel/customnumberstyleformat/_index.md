---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: Aspose.Words för .NET
description: Anpassa dina listnivåer med egenskapen ListLevel CustomNumberStyleFormat. Ställ enkelt in unika nummerformat för förbättrad dokumentformatering.
type: docs
weight: 20
url: /sv/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Hämtar eller ställer in det anpassade numeriska formatet för den här listnivån. Till exempel: "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; set; }
```

## Exempel

Visar hur man ställer in kundnummerformat.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

doc.UpdateListLabels();

ParagraphCollection paras = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("001.", paras[0].ListLabel.LabelString);
Assert.AreEqual("0001.", paras[1].ListLabel.LabelString);
Assert.AreEqual("0002.", paras[2].ListLabel.LabelString);

paras[1].ListFormat.ListLevel.CustomNumberStyleFormat = "001, 002, 003, ...";

doc.UpdateListLabels();

Assert.AreEqual("001.", paras[0].ListLabel.LabelString);
Assert.AreEqual("001.", paras[1].ListLabel.LabelString);
Assert.AreEqual("002.", paras[2].ListLabel.LabelString);
```

Visar hur man hämtar formatet för en lista med det anpassade numeriska formatet.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Vi kan få ett värde för det angivna indexet för listobjektet.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Se även

* class [ListLevel](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
