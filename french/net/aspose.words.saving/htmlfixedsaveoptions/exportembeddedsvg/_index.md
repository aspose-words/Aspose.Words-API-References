---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words pour .NET
description: HtmlFixedSaveOptions ExportEmbeddedSvg propriété. Spécifie si les ressources SVG doivent être intégrées dans le document HTML. La valeur par défaut estvrai  en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Spécifie si les ressources SVG doivent être intégrées dans le document HTML. La valeur par défaut est`vrai` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Exemples

Montre comment déterminer où stocker les objets SVG lors de l’exportation d’un document au format HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Lorsque nous exportons un document avec des objets SVG vers .html,
// Aspose.Words peut placer ces objets à deux emplacements possibles.
// Définir l'indicateur "ExportEmbeddedSvg" sur "true" intégrera toutes les données brutes des objets SVG
// dans le HTML de sortie, à l'intérieur de <image> Mots clés.
// Définir cet indicateur sur "false" créera un fichier dans le système de fichiers local pour chaque objet SVG.
// Le HTML créera un lien vers chaque fichier en utilisant l'attribut "data" d'un <objet> étiqueter.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
