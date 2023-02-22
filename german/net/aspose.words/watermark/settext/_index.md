---
title: Watermark.SetText
second_title: Aspose.Words für .NET-API-Referenz
description: Watermark methode. Fügt Textwasserzeichen in das Dokument ein.
type: docs
weight: 40
url: /de/net/aspose.words/watermark/settext/
---
## SetText(string) {#settext}

Fügt Textwasserzeichen in das Dokument ein.

```csharp
public void SetText(string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| text | String | Text, der als Wasserzeichen angezeigt wird. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn die Textlänge außerhalb des zulässigen Bereichs liegt oder der Text nur Leerzeichen enthält. |
| ArgumentNullException | Wird ausgelöst, wenn der Text null ist. |

### Bemerkungen

Die Textlänge muss im Bereich von 1 bis einschließlich 200 liegen. Der Text darf nicht null sein oder nur Leerzeichen enthalten.

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

---

## SetText(string, TextWatermarkOptions) {#settext_1}

Fügt Textwasserzeichen in das Dokument ein.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| text | String | Text, der als Wasserzeichen angezeigt wird. |
| options | TextWatermarkOptions | Definiert zusätzliche Optionen für das Textwasserzeichen. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn die Textlänge außerhalb des zulässigen Bereichs liegt oder der Text nur Leerzeichen enthält. |
| ArgumentNullException | Wird ausgelöst, wenn der Text null ist. |

### Bemerkungen

Die Textlänge muss im Bereich von 1 bis einschließlich 200 liegen. Der Text darf nicht null sein oder nur Leerzeichen enthalten.

Wenn[`TextWatermarkOptions`](../../textwatermarkoptions/) null ist, wird das Wasserzeichen mit Standardoptionen gesetzt.

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

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* namensraum [Aspose.Words](../../watermark/)
* Montage [Aspose.Words](../../../)


