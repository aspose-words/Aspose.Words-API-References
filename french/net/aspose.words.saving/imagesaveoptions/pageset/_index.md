---
title: ImageSaveOptions.PageSet
second_title: Référence de l'API Aspose.Words pour .NET
description: ImageSaveOptions propriété. Obtient ou définit les pages à afficher. La valeur par défaut est toutes les pages du document.
type: docs
weight: 90
url: /fr/net/aspose.words.saving/imagesaveoptions/pageset/
---
## ImageSaveOptions.PageSet property

Obtient ou définit les pages à afficher. La valeur par défaut est toutes les pages du document.

```csharp
public PageSet PageSet { get; set; }
```

### Remarques

Cette propriété n'a d'effet que lors du rendu des pages de document. Cette propriété est ignorée lors du rendu des formes en images.

### Exemples

Montre comment extraire des pages en fonction de plages de pages exactes.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

Montre comment rendre chaque page d'un document dans une image TIFF distincte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crée un objet "ImageSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Définissez la propriété "PageSet" sur le numéro de la première page à partir de
    // à partir duquel commencer le rendu du document.
    options.PageSet = new PageSet(i);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Montre comment spécifier la page d'un document à afficher sous forme d'image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world! This is page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 3.");

Assert.AreEqual(3, doc.PageCount);

// Lorsque nous enregistrons le document en tant qu'image, Aspose.Words n'affiche que la première page par défaut.
// Nous pouvons passer un objet SaveOptions pour spécifier une autre page à afficher.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Gif);

// Affiche chaque page du document dans un fichier image séparé.
for (int i = 1; i <= doc.PageCount; i++)
{
    saveOptions.PageSet = new PageSet(1);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageIndex.Page {i}.gif", saveOptions);
}
```

Montre comment rendre une page d'un document en une image JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crée un objet "ImageSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// Définissez le "PageSet" sur "1" pour sélectionner la deuxième page via
// l'index de base zéro à partir duquel démarrer le rendu du document.
options.PageSet = new PageSet(1);

// Lorsque nous enregistrons le document au format JPEG, Aspose.Words n'affiche qu'une seule page.
// Cette image contiendra une page à partir de la page deux,
// qui ne sera que la deuxième page du document original.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Voir également

* class [PageSet](../../pageset/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../imagesaveoptions/)
* Assemblée [Aspose.Words](../../../)


