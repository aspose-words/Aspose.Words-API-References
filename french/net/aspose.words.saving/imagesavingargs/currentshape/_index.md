---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageSavingArgs CurrentShape pour accéder à l'objet ShapeBase pour une sauvegarde efficace des formes et des groupes de formes dans vos projets.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Obtient le[`ShapeBase`](../../../aspose.words.drawing/shapebase/) objet correspondant à la forme ou au groupe de formes qui est sur le point d'être enregistré.

```csharp
public ShapeBase CurrentShape { get; }
```

## Remarques

[`IImageSavingCallback`](../../iimagesavingcallback/) peut être déclenché lors de l'enregistrement d'une forme ou d'une forme de groupe. C'est pourquoi la propriété a[`ShapeBase`](../../../aspose.words.drawing/shapebase/) type. Vous pouvez vérifier s'il s'agit d'une forme de groupe en comparant [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) avecGroup ou en le convertissant en l'une des classes dérivées : [`Shape`](../../../aspose.words.drawing/shape/) ou[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words utilise le nom du fichier du document et un numéro unique pour générer un nom de fichier unique pour chaque image trouvée dans le document. Vous pouvez utiliser l'option`CurrentShape`propriété pour générer un « meilleur » nom de fichier en examinant les propriétés de forme telles que[`Title`](../../../aspose.words.drawing/imagedata/title/) (Forme uniquement),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Forme uniquement) et[`Name`](../../../aspose.words.drawing/shapebase/name/). Bien sûr, vous pouvez créer des noms de fichiers en utilisant d'autres propriétés ou critères , mais notez que les noms de fichiers subsidiaires doivent être uniques dans l'opération d'exportation.

Certaines images du document peuvent être indisponibles. Pour vérifier la disponibilité des images, utilisez le[`IsImageAvailable`](../isimageavailable/) propriété.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
