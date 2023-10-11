---
title: TextWatermarkOptions.Color
second_title: Aspose.Words für .NET-API-Referenz
description: TextWatermarkOptions eigendom. Ruft die Schriftfarbe ab oder legt sie fest. Der Standardwert istSilver .
type: docs
weight: 20
url: /de/net/aspose.words/textwatermarkoptions/color/
---
## TextWatermarkOptions.Color property

Ruft die Schriftfarbe ab oder legt sie fest. Der Standardwert istSilver .

```csharp
public Color Color { get; set; }
```

### Beispiele

Zeigt, wie man ein Textwasserzeichen erstellt.

```csharp
Document doc = new Document();

// Ein reines Textwasserzeichen hinzufügen.
doc.Watermark.SetText("Aspose Watermark");

// Wenn wir die Textformatierung bearbeiten und ihn als Wasserzeichen verwenden möchten,
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


