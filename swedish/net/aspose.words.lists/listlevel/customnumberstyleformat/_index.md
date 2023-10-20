---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: Aspose.Words för .NET
description: ListLevel CustomNumberStyleFormat fast egendom. Hämtar det anpassade nummerformatet för denna listnivå. Till exempel a ç ĝ  i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Hämtar det anpassade nummerformatet för denna listnivå. Till exempel: "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; }
```

## Exempel

Visar hur du får formatet för en lista med den anpassade nummerstilen.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Vi kan få värde för det angivna indexet för listobjektet.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Se även

* class [ListLevel](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
