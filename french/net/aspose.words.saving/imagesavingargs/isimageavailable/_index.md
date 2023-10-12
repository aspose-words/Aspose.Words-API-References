---
title: ImageSavingArgs.IsImageAvailable
second_title: Référence de l'API Aspose.Words pour .NET
description: ImageSavingArgs propriété. Retoursvrai si limage actuelle est disponible pour lexportation.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

Retours`vrai` si l'image actuelle est disponible pour l'exportation.

```csharp
public bool IsImageAvailable { get; }
```

### Remarques

Certaines images du document peuvent être indisponibles, par exemple parce que l'image est liée et que le lien est inaccessible ou ne pointe pas vers une image valide. Dans ce cas, Aspose.Words exporte une icône avec une croix rouge. Cette propriété renvoie `vrai` si l'image originale est disponible ; Retour`FAUX`si l'image originale n'est pas disponible et une icône « pas d'image » sera proposée pour la sauvegarde.

Lors de l'enregistrement d'une forme de groupe ou d'une forme qui ne nécessite aucune image, cette propriété est toujours`vrai`.

### Exemples

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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../imagesavingargs/)
* Assemblée [Aspose.Words](../../../)


