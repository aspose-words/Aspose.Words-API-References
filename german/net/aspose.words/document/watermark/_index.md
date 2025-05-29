---
title: Document.Watermark
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words für .NET
description: Schützen Sie Ihre Dokumente mit unserer anpassbaren Wasserzeichenfunktion. Erhöhen Sie mühelos den Schutz und gewährleisten Sie Authentizität!
type: docs
weight: 500
url: /de/net/aspose.words/document/watermark/
---
## Document.Watermark property

Bietet Zugriff auf das Dokumentwasserzeichen.

```csharp
public Watermark Watermark { get; }
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

* class [Watermark](../../watermark/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
