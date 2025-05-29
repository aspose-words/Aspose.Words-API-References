---
title: ImageSavingArgs.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Document ImageSavingArgs pour accéder au document en cours d'enregistrement, améliorant ainsi l'efficacité de votre flux de travail et vous faisant gagner du temps.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/imagesavingargs/document/
---
## ImageSavingArgs.Document property

Obtient l'objet document en cours d'enregistrement.

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [ImageSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
