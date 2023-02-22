---
title: Enum WatermarkLayout
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.WatermarkLayout opsomming. Definiert das Layout des Wasserzeichens relativ zum Zentrum des Wasserzeichens.
type: docs
weight: 6370
url: /de/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

Definiert das Layout des Wasserzeichens relativ zum Zentrum des Wasserzeichens.

```csharp
public enum WatermarkLayout
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | `0` | Horizontales Wasserzeichen-Layout. Entspricht 0 Grad Rotation. |
| Diagonal | `315` | Diagonales Wasserzeichen-Layout. Entspricht 315 Grad Rotation. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


