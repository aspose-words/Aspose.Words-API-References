---
title: Watermark.Remove
second_title: Aspose.Words für .NET-API-Referenz
description: Watermark methode. Entfernt das Wasserzeichen.
type: docs
weight: 20
url: /de/net/aspose.words/watermark/remove/
---
## Watermark.Remove method

Entfernt das Wasserzeichen.

```csharp
public void Remove()
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

* class [Watermark](../)
* namensraum [Aspose.Words](../../watermark/)
* Montage [Aspose.Words](../../../)


