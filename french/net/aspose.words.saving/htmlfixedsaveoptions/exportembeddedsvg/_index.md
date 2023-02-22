---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlFixedSaveOptions propriété. Spécifie si les ressources SVG doivent être intégrées dans le document HTML. La valeur par défaut estvrai .
type: docs
weight: 70
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Spécifie si les ressources SVG doivent être intégrées dans le document HTML. La valeur par défaut est`vrai` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

### Exemples

Montre comment déterminer où stocker les objets SVG lors de l'exportation d'un document vers Html.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Lorsque nous exportons un document avec des objets SVG vers .html,
// Aspose.Words peut placer ces objets dans deux emplacements possibles.
// Définir le drapeau "ExportEmbeddedSvg" sur "true" intégrera toutes les données brutes de l'objet SVG
// dans le HTML de sortie, à l'intérieur de <image> Mots clés.
// Définir cet indicateur sur "false" créera un fichier dans le système de fichiers local pour chaque objet SVG.
// Le HTML créera un lien vers chaque fichier en utilisant l'attribut "data" d'un <object> étiquette.
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
* espace de noms [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* Assemblée [Aspose.Words](../../../)


