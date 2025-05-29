---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words pour .NET
description: Optimisez l'économie d'EMF avec ImageSaveOptions. Contrôlez les paramètres de rendu GDI ou Aspose.Words pour une qualité d'image et des performances améliorées.
type: docs
weight: 190
url: /fr/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Obtient ou définit une valeur déterminant s'il faut utiliser le moteur de rendu de métafichier GDI+ ou Aspose.Words lors de l'enregistrement au format EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Remarques

Si défini sur`vrai` Le moteur de rendu de métafichier GDI+ est utilisé. Autrement dit, le contenu est écrit dans l'objet GDI+ graphics et enregistré dans le métafichier.

Si défini sur`FAUX` Le moteur de rendu de métafichier Aspose.Words est utilisé. Autrement dit, le contenu est écrit directement au format métafichier avec Aspose.Words.

N'a d'effet que lors de l'enregistrement dans EMF.

L'enregistrement GDI+ ne fonctionne que sur .NET.

La valeur par défaut est`vrai`.

## Exemples

Montre comment choisir un moteur de rendu lors de la conversion d'un document en .emf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Lorsque nous enregistrons le document en tant qu'image EMF, nous pouvons passer un objet SaveOptions pour sélectionner un moteur de rendu pour l'image.
// Si nous définissons l'indicateur « UseGdiEmfRenderer » sur « true », Aspose.Words utilisera le moteur de rendu GDI+.
// Si nous définissons l'indicateur « UseGdiEmfRenderer » sur « false », Aspose.Words utilisera son propre moteur de rendu de métafichier.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### Voir également

* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
