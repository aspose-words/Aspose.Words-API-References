---
title: SaveOptions.UseAntiAliasing
second_title: Aspose.Words für .NET-API-Referenz
description: SaveOptions eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob AntiAliasing für das Rendering verwendet werden soll oder nicht.
type: docs
weight: 190
url: /de/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob Anti-Aliasing für das Rendering verwendet werden soll oder nicht.

```csharp
public bool UseAntiAliasing { get; set; }
```

### Bemerkungen

Der Standardwert ist`FALSCH` . Wenn dieser Wert auf eingestellt ist`WAHR` Anti-Aliasing wird für das Rendering verwendet.

Diese Eigenschaft wird verwendet, wenn das Dokument in die folgenden Formate exportiert wird: Tiff ,Png ,Bmp , Jpeg ,Emf . Wenn das Dokument nach the exportiert wirdHtml ,Mhtml , Epub ,Azw3 oderMobi Formate Diese Option wird für Rasterbilder verwendet.

### Beispiele

Zeigt, wie Sie die Qualität eines gerenderten Dokuments mit SaveOptions verbessern können.

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
* namensraum [Aspose.Words.Saving](../../saveoptions/)
* Montage [Aspose.Words](../../../)


