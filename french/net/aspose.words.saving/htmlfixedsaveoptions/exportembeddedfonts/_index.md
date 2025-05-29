---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: Aspose.Words pour .NET
description: Contrôlez l'intégration des polices dans votre code HTML avec la propriété ExportEmbeddedFonts. Améliorez la qualité de vos documents tout en gérant efficacement la taille des fichiers.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Spécifie si les polices doivent être incorporées dans un document HTML au format Base64. Notez que la définition de cet indicateur peut augmenter considérablement la taille du fichier HTML de sortie.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## Exemples

Montre comment déterminer où stocker les polices intégrées lors de l'exportation d'un document au format HTML.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// Lorsque nous exportons un document avec des polices intégrées au format .html,
// Aspose.Words peut placer les polices à deux emplacements possibles.
// La définition de l'indicateur « ExportEmbeddedFonts » sur « true » stockera les données brutes des polices intégrées dans la feuille de style CSS,
// dans la propriété « url » de la règle « @font-face ». Cela peut créer un fichier de style CSS volumineux.
// et réduisez le nombre de fichiers externes que cette conversion HTML créera.
// Définir cet indicateur sur « false » créera un fichier pour chaque police.
// La feuille de style CSS sera liée à chaque fichier de police en utilisant la propriété « url » de la règle « @font-face ».
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedFonts = exportEmbeddedFonts
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(0, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(2, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
