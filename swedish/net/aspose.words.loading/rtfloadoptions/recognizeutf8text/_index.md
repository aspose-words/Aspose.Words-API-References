---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words för .NET
description: RtfLoadOptions RecognizeUtf8Text fast egendom. När inställd påSann CharsetDetector kommer att försöka upptäcka UTF8tecken de kommer att bevaras under import i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

När inställd på`Sann` ,CharsetDetector kommer att försöka upptäcka UTF8-tecken, de kommer att bevaras under import.

Standardvärdet är`falsk` .

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## Exempel

Visar hur man upptäcker UTF-8-tecken när ett RTF-dokument laddas.

```csharp
// Skapa ett "RtfLoadOptions"-objekt för att ändra hur vi laddar ett RTF-dokument.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Ställ in egenskapen "RecognizeUtf8Text" till "false" för att anta att dokumentet använder ISO 8859-1-teckenuppsättningen
// och laddar varje tecken i dokumentet.
// Ställ in egenskapen "RecognizeUtf8Text" till "true" för att analysera alla tecken med variabel längd som kan förekomma i texten.
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
