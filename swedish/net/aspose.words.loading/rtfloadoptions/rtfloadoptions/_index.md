---
title: RtfLoadOptions
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck RtfLoadOptions-konstruktorn som enkelt initierar din klass med standardvärden, vilket förbättrar din kodningseffektivitet och produktivitet.
type: docs
weight: 10
url: /sv/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

Initierar en ny instans av den här klassen med standardvärden.

```csharp
public RtfLoadOptions()
```

## Exempel

Visar hur man identifierar UTF-8-tecken när man laddar ett RTF-dokument.

```csharp
// Skapa ett "RtfLoadOptions"-objekt för att ändra hur vi laddar ett RTF-dokument.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Sätt egenskapen "RecognizeUtf8Text" till "false" för att anta att dokumentet använder ISO 8859-1-teckenuppsättningen
// och laddar alla tecken i dokumentet.
// Sätt egenskapen "RecognizeUtf8Text" till "true" för att analysera eventuella tecken med variabel längd som kan förekomma i texten.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Se även

* class [RtfLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
