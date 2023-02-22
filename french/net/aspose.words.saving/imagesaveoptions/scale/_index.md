---
title: ImageSaveOptions.Scale
second_title: Référence de l'API Aspose.Words pour .NET
description: ImageSaveOptions propriété. Obtient ou définit le facteur de zoom pour les images générées.
type: docs
weight: 140
url: /fr/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

Obtient ou définit le facteur de zoom pour les images générées.

```csharp
public float Scale { get; set; }
```

### Remarques

La valeur par défaut est 1.0. La valeur doit être supérieure à 0.

### Exemples

Montre comment restituer un objet Office Math dans un fichier image dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Crée un objet "ImageSaveOptions" à passer à la méthode "Save" du rendu de nœud pour modifier
// comment il rend le nœud OfficeMath dans une image.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Définissez la propriété "Scale" sur 5 pour restituer l'objet à cinq fois sa taille d'origine.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

Montre comment modifier l'image pendant qu'Aspose.Words convertit un document en un seul.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Lorsque nous enregistrons le document en tant qu'image, nous pouvons passer un objet SaveOptions à
// édite l'image pendant que l'opération de sauvegarde la rend.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Nous pouvons ajuster ces propriétés pour modifier la luminosité et le contraste de l'image.
    // Les deux sont sur une échelle de 0 à 1 et sont à 0,5 par défaut.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Nous pouvons ajuster la résolution horizontale et verticale avec ces propriétés.
    // Cela affectera les dimensions de l'image.
    // La valeur par défaut de ces propriétés est 96.0, pour une résolution de 96dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Nous pouvons redimensionner l'image en utilisant cette propriété. La valeur par défaut est 1,0, pour une mise à l'échelle de 100 %.
    // Nous pouvons utiliser cette propriété pour annuler tout changement dans les dimensions de l'image que le changement de résolution entraînerait.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Voir également

* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../imagesaveoptions/)
* Assemblée [Aspose.Words](../../../)


