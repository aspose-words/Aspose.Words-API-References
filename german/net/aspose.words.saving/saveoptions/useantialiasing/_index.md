---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveOptions UseAntiAliasing-Eigenschaft, um Ihre Rendering-Qualität zu verbessern. Steuern Sie Antialiasing für eine flüssigere Darstellung und verbesserte Leistung.
type: docs
weight: 200
url: /de/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Anti-Aliasing zum Rendern verwendet werden soll oder nicht.

```csharp
public bool UseAntiAliasing { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` Wenn dieser Wert auf`WAHR` Anti-Aliasing wird zum Rendern verwendet.

Diese Eigenschaft wird verwendet, wenn das Dokument in die folgenden Formate exportiert wird: Tiff ,Png ,Bmp , Jpeg ,Emf . Wenn das Dokument in das exportiert wirdHtml ,Mhtml , Epub ,Azw3 oderMobiFormate: Diese Option wird für Rasterbilder verwendet.

## Beispiele

Zeigt, wie die Qualität eines gerenderten Dokuments mit SaveOptions verbessert werden kann.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
