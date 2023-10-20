---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words pour .NET
description: HtmlFixedSaveOptions ExportEmbeddedCss propriété. Spécifie si le CSS Cascading Style Sheet doit être intégré dans le document HTML en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

Spécifie si le CSS (Cascading Style Sheet) doit être intégré dans le document HTML.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## Exemples

Montre comment déterminer où stocker les feuilles de style CSS lors de l’exportation d’un document au format HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Lorsque nous exportons un document au format HTML, Aspose.Words créera également une feuille de style CSS pour formater le document.
// Définition du flag "ExportEmbeddedCss" sur "true" enregistre la feuille de style CSS dans un fichier .css,
// et créez un lien vers le fichier à partir du document HTML à l'aide d'un <link> élément.
// Définir l'indicateur sur "false" intégrera la feuille de style CSS dans le document HTML,
// qui ne créera qu'un seul fichier au lieu de deux.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.True(Regex.Match(outDocContents, "<style type=\"text/css\">").Success);
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success);
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
