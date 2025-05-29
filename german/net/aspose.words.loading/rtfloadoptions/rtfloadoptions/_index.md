---
title: RtfLoadOptions
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den RtfLoadOptions-Konstruktor, der Ihre Klasse mühelos mit Standardwerten initialisiert und so Ihre Codierungseffizienz und Produktivität steigert.
type: docs
weight: 10
url: /de/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```csharp
public RtfLoadOptions()
```

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
