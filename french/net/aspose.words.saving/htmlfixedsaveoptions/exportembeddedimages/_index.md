---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ExportEmbeddedImages dans HtmlFixedSaveOptions améliore vos documents HTML en incorporant des images au format Base64, optimisant la qualité visuelle tout en gérant la taille du fichier.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Spécifie si les images doivent être incorporées dans un document HTML au format Base64. Notez que la définition de cet indicateur peut augmenter considérablement la taille du fichier HTML de sortie.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Exemples

Montre comment déterminer où stocker les images lors de l'exportation d'un document au format HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Lorsque nous exportons un document avec des images intégrées au format .html,
// Aspose.Words peut placer les images à deux emplacements possibles.
// La définition de l'indicateur « ExportEmbeddedImages » sur « true » stockera les données brutes
// pour toutes les images dans le document HTML de sortie, dans l'attribut « src » des balises <image>.
// Définir cet indicateur sur « false » créera un fichier image dans le système de fichiers local pour chaque image,
// et stockez tous ces fichiers dans un dossier séparé.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedImages = exportImages
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
        "src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />").Success);
}
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
