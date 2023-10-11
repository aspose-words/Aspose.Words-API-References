---
title: TextWatermarkOptions.FontSize
second_title: Aspose.Words für .NET-API-Referenz
description: TextWatermarkOptions eigendom. Ruft eine Schriftgröße ab oder legt diese fest. Der Standardwert ist 0  auto.
type: docs
weight: 40
url: /de/net/aspose.words/textwatermarkoptions/fontsize/
---
## TextWatermarkOptions.FontSize property

Ruft eine Schriftgröße ab oder legt diese fest. Der Standardwert ist 0 - auto.

```csharp
public float FontSize { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des gültigen Wertebereichs lag. |

### Bemerkungen

Gültige Werte liegen zwischen 0 und 65,5.

Automatische Schriftgröße bedeutet, dass das Wasserzeichen auf seine maximale Breite und maximale Höhe relativ zu den Seitenrändern skaliert wird.

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


