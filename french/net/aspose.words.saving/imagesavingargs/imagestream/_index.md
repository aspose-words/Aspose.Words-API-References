---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words pour .NET
description: ImageSavingArgs ImageStream propriété. Permet de spécifier le flux dans lequel limage sera enregistrée en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Permet de spécifier le flux dans lequel l'image sera enregistrée.

```csharp
public Stream ImageStream { get; set; }
```

## Remarques

Cette propriété vous permet d'enregistrer des images dans des flux plutôt que dans des fichiers HTML.

La valeur par défaut est`nul` . Lorsque cette propriété est`nul` , l'image sera enregistrée dans un fichier spécifié dans le[`ImageFileName`](../imagefilename/) propriété.

En utilisant[`IImageSavingCallback`](../../iimagesavingcallback/) vous ne pouvez pas remplacer une image par une autre. Il est destiné uniquement au contrôle de l'emplacement où enregistrer les images.

## Exemples

Montre comment impliquer un rappel d’enregistrement d’image dans un processus de conversion HTML.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions pour désigner un rappel
    // pour personnaliser le processus de sauvegarde de l'image.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Imprime les propriétés de chaque image au fur et à mesure que le processus d'enregistrement l'enregistre dans un fichier image dans le système de fichiers local
/// lors de l'export d'un document au format HTML.
/// </summary>
private class ImageShapePrinter : IImageSavingCallback
{
    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        args.KeepImageStreamOpen = false;
        Assert.True(args.IsImageAvailable);

        Console.WriteLine($"{args.Document.OriginalFileName.Split('\\').Last()} Image #{++mImageCount}");

        LayoutCollector layoutCollector = new LayoutCollector(args.Document);

        Console.WriteLine($"\tOn page:\t{layoutCollector.GetStartPageIndex(args.CurrentShape)}");
        Console.WriteLine($"\tDimensions:\t{args.CurrentShape.Bounds}");
        Console.WriteLine($"\tAlignment:\t{args.CurrentShape.VerticalAlignment}");
        Console.WriteLine($"\tWrap type:\t{args.CurrentShape.WrapType}");
        Console.WriteLine($"Output filename:\t{args.ImageFileName}\n");
    }

    private int mImageCount;
}
```

### Voir également

* class [ImageSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
