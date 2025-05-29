---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.WatermarkType zur einfachen Anpassung von Wasserzeichen in Dokumenten. Optimieren Sie Ihre Projekte mit vielseitigen Wasserzeichenoptionen!
type: docs
weight: 7540
url: /de/net/aspose.words/watermarktype/
---
## WatermarkType enumeration

Gibt den Wasserzeichentyp an.

```csharp
public enum WatermarkType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | `0` | Gibt an, dass der Text als Wasserzeichen verwendet wird. |
| Image | `1` | Gibt an, dass das Bild als Wasserzeichen verwendet wird. |
| None | `2` | Zeigt an, dass kein Wasserzeichen festgelegt ist. |

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
