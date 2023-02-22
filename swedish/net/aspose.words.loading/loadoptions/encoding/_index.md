---
title: LoadOptions.Encoding
second_title: Aspose.Words för .NET API Referens
description: LoadOptions fast egendom. Hämtar eller ställer in kodningen som ska användas för att ladda ett HTML TXT eller CHMdokument om kodningen inte är specificerad inuti dokumentet. Kan vara null. Standard är null.
type: docs
weight: 50
url: /sv/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Hämtar eller ställer in kodningen som ska användas för att ladda ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad inuti dokumentet. Kan vara null. Standard är null.

```csharp
public Encoding Encoding { get; set; }
```

### Anmärkningar

Den här egenskapen används endast när HTML-, TXT- eller CHM-dokument laddas.

Om kodning inte anges i dokumentet och den här egenskapen är`null`, då kommer systemet att försöka automatiskt upptäcka kodningen.

### Exempel

Visar hur man ställer in kodningen för att öppna ett dokument.

```csharp
// Ett FileFormatInfo-objekt kommer att upptäcka den här filen som kodad i något annat än UTF-7.
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Encoded in UTF-7.txt");

Assert.AreNotEqual(Encoding.UTF7, fileFormatInfo.Encoding);

// Om vi laddar dokumentet utan laddningskonfigurationer kommer Aspose.Words att upptäcka dess kodning som UTF-8.
Document doc = new Document(MyDir + "Encoded in UTF-7.txt");

// Innehållet, analyserat i UTF-8, skapar en giltig sträng.
// Men när vi vet att filen är i UTF-7 kan vi se att resultatet är felaktigt.
Assert.AreEqual("Hello world+ACE-", doc.ToString(SaveFormat.Text).Trim());

// I fall av tvetydig kodning som den här, kan vi ställa in en specifik kodningsvariant
// för att analysera filen i ett LoadOptions-objekt.
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.UTF7
};

// Ladda dokumentet medan du skickar LoadOptions-objektet och verifiera sedan dokumentets innehåll.
doc = new Document(MyDir + "Encoded in UTF-7.txt", loadOptions);

Assert.AreEqual("Hello world!", doc.ToString(SaveFormat.Text).Trim());
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../loadoptions/)
* hopsättning [Aspose.Words](../../../)


