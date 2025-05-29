---
title: TextWatermarkOptions.Layout
linktitle: Layout
articleTitle: Layout
second_title: Aspose.Words für .NET
description: Entdecken Sie die Layout-Eigenschaft von TextWatermarkOptions, um das Erscheinungsbild Ihres Wasserzeichens anzupassen. Stellen Sie es einfach auf Diagonal oder Ihr bevorzugtes Layout für eine verbesserte Optik ein.
type: docs
weight: 60
url: /de/net/aspose.words/textwatermarkoptions/layout/
---
## TextWatermarkOptions.Layout property

Ruft das Layout des Wasserzeichens ab oder legt es fest. Der Standardwert istDiagonal .

```csharp
public WatermarkLayout Layout { get; set; }
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

* enum [WatermarkLayout](../../watermarklayout/)
* class [TextWatermarkOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
