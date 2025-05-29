---
title: TextWatermarkOptions.IsSemitrasparent
linktitle: IsSemitrasparent
articleTitle: IsSemitrasparent
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „IsSemitransparent“ von TextWatermarkOptions – steuern Sie die Deckkraft von Wasserzeichen ganz einfach. Verbessern Sie Ihre Designs mit anpassbaren Transparenzeinstellungen!
type: docs
weight: 50
url: /de/net/aspose.words/textwatermarkoptions/issemitrasparent/
---
## TextWatermarkOptions.IsSemitrasparent property

Ruft einen booleschen Wert ab oder legt ihn fest, der für die Deckkraft des Wasserzeichens verantwortlich ist. Der Standardwert ist`WAHR` .

```csharp
public bool IsSemitrasparent { get; set; }
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
