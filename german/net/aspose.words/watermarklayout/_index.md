---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.WatermarkLayout-Aufzählung für optimale Wasserzeichenpositionierung. Verbessern Sie Ihr Dokumentdesign mit präziser Layoutsteuerung und -anpassung.
type: docs
weight: 7530
url: /de/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

Definiert das Layout des Wasserzeichens relativ zur Wasserzeichenmitte.

```csharp
public enum WatermarkLayout
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | `0` | Horizontales Wasserzeichenlayout. Entspricht 0 Grad Drehung. |
| Diagonal | `315` | Diagonales Wasserzeichenlayout. Entspricht einer Drehung von 315 Grad. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
