---
title: TextWatermarkOptions.FontFamily
second_title: Aspose.Words für .NET-API-Referenz
description: TextWatermarkOptions eigendom. Ruft den Namen der Schriftfamilie ab oder legt ihn fest. Der Standardwert ist Calibri.
type: docs
weight: 30
url: /de/net/aspose.words/textwatermarkoptions/fontfamily/
---
## TextWatermarkOptions.FontFamily property

Ruft den Namen der Schriftfamilie ab oder legt ihn fest. Der Standardwert ist "Calibri".

```csharp
public string FontFamily { get; set; }
```

### Beispiele

Zeigt, wie ein Textwasserzeichen erstellt wird.

```csharp
Document doc = new Document();

// Fügen Sie ein Nur-Text-Wasserzeichen hinzu.
doc.Watermark.SetText("Aspose Watermark");

// Wenn wir die Textformatierung als Wasserzeichen bearbeiten möchten,
// Wir können dies tun, indem wir beim Erstellen des Wasserzeichens ein TextWatermarkOptions-Objekt übergeben.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Wir können ein Wasserzeichen aus einem Dokument wie diesem entfernen.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Siehe auch

* class [TextWatermarkOptions](../)
* namensraum [Aspose.Words](../../textwatermarkoptions/)
* Montage [Aspose.Words](../../../)


