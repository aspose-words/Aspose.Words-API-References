---
title: ImageSavingArgs.KeepImageStreamOpen
linktitle: KeepImageStreamOpen
articleTitle: KeepImageStreamOpen
second_title: Aspose.Words pour .NET
description: Découvrez la propriété KeepImageStreamOpen dans ImageSavingArgs pour Aspose.Words. Contrôlez le comportement du flux pour une sauvegarde efficace des images et des performances améliorées.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une image.

```csharp
public bool KeepImageStreamOpen { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` et Aspose.Words fermera le flux que vous avez fourni dans le[`ImageStream`](../imagestream/) propriété après avoir écrit une image dedans. Spécifier`vrai` pour garder le ruisseau ouvert.

## Exemples

Montre comment impliquer un rappel d'enregistrement d'image dans un processus de conversion HTML.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions pour désigner un rappel
    // pour personnaliser le processus d'enregistrement de l'image.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Imprime les propriétés de chaque image lorsque le processus d'enregistrement l'enregistre dans un fichier image dans le système de fichiers local
/// lors de l'exportation d'un document au format HTML.
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
