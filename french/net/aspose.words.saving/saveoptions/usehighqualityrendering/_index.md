---
title: SaveOptions.UseHighQualityRendering
linktitle: UseHighQualityRendering
articleTitle: UseHighQualityRendering
second_title: Aspose.Words pour .NET
description: SaveOptions UseHighQualityRendering propriété. Obtient ou définit une valeur déterminant sil faut ou non utiliser des algorithmes de rendu de haute qualité cestàdire lents en C#.
type: docs
weight: 200
url: /fr/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents).

```csharp
public bool UseHighQualityRendering { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

Cette propriété est utilisée lorsque le document est exporté aux formats d'image : Tiff ,Png ,Bmp , Jpeg ,Emf.

## Exemples

Montre comment améliorer la qualité d’un document rendu avec SaveOptions.

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

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
