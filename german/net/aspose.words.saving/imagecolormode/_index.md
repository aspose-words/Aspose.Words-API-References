---
title: ImageColorMode Enum
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Saving.ImageColorMode zur Optimierung von Dokumentseitenbildern. Steuern Sie die Farbmodi für eine verbesserte visuelle Qualität Ihrer Projekte.
type: docs
weight: 5960
url: /de/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

Gibt den Farbmodus für die generierten Bilder der Dokumentseiten an.

```csharp
public enum ImageColorMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Die Seiten des Dokuments werden als Farbbilder gerendert. |
| Grayscale | `1` | Die Seiten des Dokuments werden als Graustufenbilder gerendert. |
| BlackAndWhite | `2` | Die Seiten des Dokuments werden als Schwarzweißbilder gerendert. |

## Beispiele

Zeigt, wie beim Rendern von Dokumenten ein Farbmodus festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben an
// Wählen Sie einen Farbmodus für das Bild aus, das beim Speichern generiert wird.
// Wenn wir die Eigenschaft "ImageColorMode" auf "ImageColorMode.BlackAndWhite" setzen,
// Beim Speichern wird beim Rendern des Dokuments eine Graustufenfarbreduzierung angewendet.
    // Wenn wir die Eigenschaft "ImageColorMode" auf "ImageColorMode.Grayscale" setzen,
// Durch den Speichervorgang wird das Dokument in ein monochromes Bild umgewandelt.
// Wenn wir die Eigenschaft „ImageColorMode“ auf „None“ setzen, wird beim Speichern die Standardmethode angewendet
// und alle Farben des Dokuments im Ausgabebild beibehalten.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
