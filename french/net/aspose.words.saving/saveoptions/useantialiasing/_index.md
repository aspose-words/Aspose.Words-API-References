---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SaveOptions UseAntiAliasing pour améliorer la qualité de votre rendu. Contrôlez l'anticrénelage pour des visuels plus fluides et des performances améliorées.
type: docs
weight: 200
url: /fr/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu.

```csharp
public bool UseAntiAliasing { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` . Lorsque cette valeur est définie sur`vrai` l'anticrénelage est utilisé pour le rendu.

Cette propriété est utilisée lorsque le document est exporté vers les formats suivants : Tiff ,Png ,Bmp , Jpeg ,Emf . Lorsque le document est exporté vers the Html ,Mhtml , Epub ,Azw3 ouMobiformats cette option est utilisée pour les images raster.

## Exemples

Montre comment améliorer la qualité d'un document rendu avec SaveOptions.

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
