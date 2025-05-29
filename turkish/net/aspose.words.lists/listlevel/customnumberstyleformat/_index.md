---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: .NET için Aspose.Words
description: ListLevel CustomNumberStyleFormat özelliğiyle liste düzeylerinizi özelleştirin. Gelişmiş belge stili için benzersiz sayı biçimlerini kolayca ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Bu liste düzeyi için özel sayı stili biçimini alır veya ayarlar. Örneğin: "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; set; }
```

## Örnekler

Müşteri numarası stil formatının nasıl ayarlanacağını gösterir.

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

Özel sayı stiline sahip bir listenin biçiminin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Liste öğesinin belirtilen indeksine ait değeri alabiliriz.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Ayrıca bakınız

* class [ListLevel](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
