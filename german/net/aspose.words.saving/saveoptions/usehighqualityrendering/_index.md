---
title: SaveOptions.UseHighQualityRendering
linktitle: UseHighQualityRendering
articleTitle: UseHighQualityRendering
second_title: Aspose.Words für .NET
description: SaveOptions UseHighQualityRendering eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob hochwertige d. h. langsame RenderingAlgorithmen verwendet werden sollen oder nicht in C#.
type: docs
weight: 200
url: /de/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob hochwertige (d. h. langsame) Rendering-Algorithmen verwendet werden sollen oder nicht.

```csharp
public bool UseHighQualityRendering { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

Diese Eigenschaft wird verwendet, wenn das Dokument in Bildformate exportiert wird: Tiff ,Png ,Bmp , Jpeg ,Emf.

## Beispiele

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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
