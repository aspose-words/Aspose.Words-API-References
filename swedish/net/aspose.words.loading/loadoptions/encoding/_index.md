---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LoadOptions Encoding för att enkelt hantera HTML TXT- eller CHM-dokumentkodning. Anpassa din innehållsinläsning för optimal prestanda!
type: docs
weight: 50
url: /sv/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara`null` Standard är`null` .

```csharp
public Encoding Encoding { get; set; }
```

## Anmärkningar

Den här egenskapen används endast vid laddning av HTML-, TXT- eller CHM-dokument.

Om kodning inte anges i dokumentet och den här egenskapen är`null`då kommer systemet att försöka att automatiskt upptäcka kodningen.

## Exempel

Visar hur man ställer in kodningen för att öppna ett dokument.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// Ladda dokumentet medan LoadOptions-objektet skickas, verifiera sedan dokumentets innehåll.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
