---
title: UseHighQualityRendering
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft einen Wert ab oder legt ihn fest der bestimmt ob qualitativ hochwertige dh langsame Renderalgorithmen verwendet werden sollen oder nicht.
type: docs
weight: 220
url: /de/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (dh langsame) Renderalgorithmen verwendet werden sollen oder nicht.

```csharp
public bool UseHighQualityRendering { get; set; }
```

### Bemerkungen

Der Standardwert ist`FALSCH` .

Diese Eigenschaft wird verwendet, wenn das Dokument in Bildformate exportiert wird: Tiff ,Png ,Bmp , Jpeg ,Emf.

### Beispiele

Zeigt, wie die Qualität eines gerenderten Dokuments mit SaveOptions verbessert wird.

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

* class [SaveOptions](../../saveoptions)
* namensraum [Aspose.Words.Saving](../../saveoptions)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
