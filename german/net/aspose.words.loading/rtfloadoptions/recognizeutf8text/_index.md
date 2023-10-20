---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words für .NET
description: RtfLoadOptions RecognizeUtf8Text eigendom. Wenn eingestellt aufWAHR CharsetDetector wird versuchen UTF8Zeichen zu erkennen sie bleiben beim Import erhalten in C#.
type: docs
weight: 20
url: /de/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

Wenn eingestellt auf`WAHR` ,CharsetDetector wird versuchen, UTF8-Zeichen zu erkennen, sie bleiben beim Import erhalten.

Der Standardwert ist`FALSCH` .

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## Beispiele

Zeigt, wie UTF-8-Zeichen beim Laden eines RTF-Dokuments erkannt werden.

```csharp
// Erstellen Sie ein „RtfLoadOptions“-Objekt, um zu ändern, wie wir ein RTF-Dokument laden.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Setzen Sie die Eigenschaft „RecognizeUtf8Text“ auf „false“, um anzunehmen, dass das Dokument den ISO 8859-1-Zeichensatz verwendet
// und lädt jedes Zeichen im Dokument.
// Setzen Sie die Eigenschaft „RecognizeUtf8Text“ auf „true“, um alle Zeichen variabler Länge zu analysieren, die im Text vorkommen können.
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

### Siehe auch

* class [RtfLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
