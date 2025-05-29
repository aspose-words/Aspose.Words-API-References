---
title: TextWatermarkOptions.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words für .NET
description: Passen Sie Ihre TextWatermarkOptions mit der Eigenschaft „Farbe“ an, um die Sichtbarkeit zu verbessern. Wählen Sie Ihre bevorzugte Schriftfarbe für eine persönliche Note. Standardmäßig: Silber.
type: docs
weight: 20
url: /de/net/aspose.words/textwatermarkoptions/color/
---
## TextWatermarkOptions.Color property

Ruft die Schriftfarbe ab oder legt sie fest. Der Standardwert istSilver .

```csharp
public Color Color { get; set; }
```

## Beispiele

Zeigt, wie ein Textwasserzeichen erstellt wird.

```csharp
Document doc = new Document();

// Fügen Sie ein Wasserzeichen im Klartext hinzu.
doc.Watermark.SetText("Aspose Watermark");

// Wenn wir die Textformatierung bearbeiten und sie als Wasserzeichen verwenden möchten,
// Dies können wir tun, indem wir beim Erstellen des Wasserzeichens ein TextWatermarkOptions-Objekt übergeben.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
