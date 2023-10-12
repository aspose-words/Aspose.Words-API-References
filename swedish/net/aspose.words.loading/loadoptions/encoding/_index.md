---
title: LoadOptions.Encoding
second_title: Aspose.Words för .NET API Referens
description: LoadOptions fast egendom. Hämtar eller ställer in kodningen som ska användas för att ladda ett HTML TXT eller CHMdokument om kodningen inte är specificerad inuti dokumentet. Kan varanull . Standard ärnull .
type: docs
weight: 50
url: /sv/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Hämtar eller ställer in kodningen som ska användas för att ladda ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad inuti dokumentet. Kan vara`null` . Standard är`null` .

```csharp
public Encoding Encoding { get; set; }
```

### Anmärkningar

Den här egenskapen används endast när HTML-, TXT- eller CHM-dokument laddas.

Om kodning inte anges i dokumentet och den här egenskapen är`null`då kommer systemet att försöka automatiskt upptäcka kodningen.

### Exempel

Visar hur man ställer in kodningen för att öppna ett dokument.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// Ladda dokumentet medan du skickar LoadOptions-objektet och verifiera sedan dokumentets innehåll.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../loadoptions/)
* hopsättning [Aspose.Words](../../../)


