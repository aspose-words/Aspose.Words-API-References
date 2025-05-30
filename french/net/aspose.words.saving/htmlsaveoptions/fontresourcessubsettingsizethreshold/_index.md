---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words pour .NET
description: Optimisez vos fichiers HTML, MHTML ou EPUB avec la propriété FontResourcesSubsettingSizeThreshold, garantissant une gestion efficace des ressources de polices. Valeur par défaut  0.
type: docs
weight: 290
url: /fr/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Contrôle les ressources de police qui nécessitent un sous-ensemble lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Remarques

[`ExportFontResources`](../exportfontresources/) Permet d'exporter les polices sous forme de fichiers secondaires ou de composants du package output . Si le document utilise de nombreuses polices, notamment avec un grand nombre de glyphes, la taille du fichier de sortie peut augmenter considérablement. Le sous-ensemble de polices réduit la taille de la ressource de police exportée en filtrant les glyphes non utilisés par le document actuel.

Le sous-ensemble de polices fonctionne comme suit :

* Par défaut, toutes les polices exportées sont des sous-ensembles.
* Paramètre`FontResourcesSubsettingSizeThreshold` à une valeur positive indique à Aspose.Words de sous-ensembleer les polices dont la taille de fichier est supérieure à la valeur spécifiée.
* Définition de la propriété surMaxValue supprime le sous-ensemble de polices.

**Important!**Lors de l'exportation de ressources de polices, les questions de licence doivent être prises en compte. Les auteurs souhaitant utiliser des polices spécifiques via un mécanisme de téléchargement doivent toujours vérifier soigneusement que l'utilisation prévue est conforme à la licence de police. De nombreuses polices commerciales n'autorisent actuellement pas le téléchargement web, sous quelque forme que ce soit. Les contrats de licence qui couvrent certaines polices précisent expressément que leur utilisation via**@font-face** Les règles dans les feuilles de style CSS ne sont pas autorisées. Les sous-ensembles de polices peuvent également enfreindre les conditions de licence.

## Exemples

Montre comment travailler avec un sous-ensemble de polices.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions pour configurer le sous-ensemble de polices.
// Supposons que nous définissions l'indicateur « ExportFontResources » sur « true » et que nous nommions également un dossier dans la propriété « FontsFolder ».
// Dans ce cas, l'opération de sauvegarde créera ce dossier et placera un fichier .ttf à l'intérieur
// ce dossier pour chaque police utilisée par notre document.
// Chaque fichier .ttf contiendra l'ensemble des glyphes de cette police,
// ce qui peut potentiellement donner lieu à un fichier très volumineux qui accompagne le document.
// Lorsque nous appliquons un sous-ensemble à une police, ses données brutes exportées ne contiendront que les glyphes que le document contient.
// en utilisant plutôt l'ensemble des glyphes. Si le texte de notre document n'utilise qu'une petite fraction de la police
// ensemble de glyphes, puis le sous-ensemble réduira considérablement la taille de nos documents de sortie.
// Nous pouvons utiliser la propriété « FontResourcesSubsettingSizeThreshold » pour définir une taille de fichier .ttf, en octets.
 // Si une police exportée crée un fichier de taille supérieure à celle-ci, l'opération de sauvegarde appliquera un sous-ensemble à cette police.
// La définition d'un seuil de 0 applique le sous-ensemble à toutes les polices,
// et le définir sur « int.MaxValue » désactive efficacement le sous-ensemble.
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.AreEqual(3, fontFileNames.Length);

foreach (string filename in fontFileNames)
{
    // Par défaut, les fichiers .ttf pour chacune de nos trois polices feront plus de 700 Mo.
    // Le sous-ensemble les réduira tous à moins de 30 Mo.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
