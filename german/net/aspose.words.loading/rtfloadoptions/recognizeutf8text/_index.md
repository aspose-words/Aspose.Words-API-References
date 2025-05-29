---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „RecognizeUtf8Text“ von RtfLoadOptions UTF-8-Zeichen während des Imports beibehält und so eine genaue Textdarstellung und nahtlose Integration gewährleistet.
type: docs
weight: 20
url: /de/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

Bei Einstellung auf`WAHR` , versucht, UTF8-Zeichen zu erkennen, sie bleiben beim Import erhalten.

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie beim Laden eines RTF-Dokuments UTF-8-Zeichen erkannt werden.

```csharp
// Erstellen Sie ein „RtfLoadOptions“-Objekt, um zu ändern, wie wir ein RTF-Dokument laden.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Setzen Sie die Eigenschaft „RecognizeUtf8Text“ auf „false“, um anzunehmen, dass das Dokument den Zeichensatz ISO 8859-1 verwendet
// und lädt jedes Zeichen im Dokument.
// Setzen Sie die Eigenschaft „RecognizeUtf8Text“ auf „true“, um alle im Text vorkommenden Zeichen variabler Länge zu analysieren.
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
