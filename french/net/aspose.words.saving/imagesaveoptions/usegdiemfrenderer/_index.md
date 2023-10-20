---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words pour .NET
description: ImageSaveOptions UseGdiEmfRenderer propriété. Obtient ou définit une valeur déterminant sil faut utiliser le moteur de rendu de métafichier GDI ou Aspose.Words lors de lenregistrement dans EMF en C#.
type: docs
weight: 190
url: /fr/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Obtient ou définit une valeur déterminant s'il faut utiliser le moteur de rendu de métafichier GDI+ ou Aspose.Words lors de l'enregistrement dans EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Remarques

Si réglé sur`vrai` Le moteur de rendu de métafichiers GDI+ est utilisé. C'est-à-dire que le contenu est écrit dans l'objet GDI+graphics et enregistré dans un métafichier.

Si réglé sur`FAUX` Le moteur de rendu de métafichier Aspose.Words est utilisé. C'est-à-dire que le contenu est écrit directement au format métafichier avec Aspose.Words.

N'a d'effet que lors de l'enregistrement dans EMF.

La sauvegarde GDI+ ne fonctionne que sur .NET.

La valeur par défaut est`vrai`.

## Exemples

Montre comment choisir un moteur de rendu lors de la conversion d'un document au format .emf.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            // Lorsque nous enregistrons le document en tant qu'image EMF, nous pouvons transmettre un objet SaveOptions pour sélectionner un moteur de rendu pour l'image.
            // Si nous définissons l'indicateur "UseGdiEmfRenderer" sur "true", Aspose.Words utilisera le moteur de rendu GDI+.
            // Si nous définissons l'indicateur "UseGdiEmfRenderer" sur "false", Aspose.Words utilisera son propre moteur de rendu de métafichier.
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
            saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);

            // Le moteur de rendu GDI+ crée généralement des fichiers plus volumineux.
            if (useGdiEmfRenderer)
#if NET48 || JAVA
                Assert.That(300000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#elif NET5_0_OR_GREATER
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#endif
            else
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
```

### Voir également

* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
