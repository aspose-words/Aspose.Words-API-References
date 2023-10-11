---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Contrôle quelles ressources de police nécessitent des sousensembles lors de lenregistrement au format HTML MHTML ou EPUB. La valeur par défaut est0 .
type: docs
weight: 290
url: /fr/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Contrôle quelles ressources de police nécessitent des sous-ensembles lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### Remarques

[`ExportFontResources`](../exportfontresources/) permet d'exporter des polices en tant que fichiers subsidiaires ou en tant que parties du package output . Si le document utilise de nombreuses polices, en particulier avec un grand nombre de glyphes, la taille de sortie peut augmenter considérablement de . Le sous-paramètre de police réduit la taille de la ressource de police exportée en filtrant les glyphes that ne sont pas utilisés par le document actuel.

Le sous-ensemble de polices fonctionne comme suit :

* Par défaut, toutes les polices exportées sont sous-ensembles.
* Paramètre`FontResourcesSubsettingSizeThreshold`à une valeur positive, demande à Aspose.Words de sous-ensembler les polices dont la taille de fichier est supérieure à la valeur spécifiée.
* Définir la propriété surMaxValue supprime le sous-ensemble de polices.

**Important!** Lors de l’exportation de ressources de polices, les problèmes de licence de polices doivent être pris en compte. Les auteurs qui souhaitent utiliser des polices spécifiques via un mécanisme de police downloadable doivent toujours vérifier soigneusement que leur utilisation prévue entre dans le cadre de la licence de police. De nombreuses polices commerciales ne permettent actuellement pas de télécharger leurs polices sur le Web sous quelque forme que ce soit. Les contrats de licence qui couvrent certaines polices indiquent spécifiquement que l'utilisation via **@font-face** Rules dans les feuilles de style CSS n'est pas autorisé. Les sous-ensembles de polices peuvent également enfreindre les termes de la licence.

### Exemples

Montre comment utiliser les sous-ensembles de polices.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Lorsque nous enregistrons le document au format HTML, nous pouvons transmettre un sous-paramètre de police de configuration d'objet SaveOptions.
// Supposons que nous définissions l'indicateur "ExportFontResources" sur "true" et que nous nommions également un dossier dans la propriété "FontsFolder".
// Dans ce cas, l'opération de sauvegarde créera ce dossier et placera un fichier .ttf à l'intérieur
// ce dossier pour chaque police utilisée par notre document.
// Chaque fichier .ttf contiendra l'intégralité du jeu de glyphes de cette police,
// ce qui peut potentiellement donner lieu à un très gros fichier accompagnant le document.
// Lorsque nous appliquons un sous-ensemble à une police, ses données brutes exportées ne contiendront que les glyphes du document
// utilisant à la place de l'ensemble des glyphes. Si le texte de notre document n'utilise qu'une petite fraction de la police
// ensemble de glyphes, puis le sous-ensemble réduira considérablement la taille de nos documents de sortie.
// On peut utiliser la propriété "FontResourcesSubsettingSizeThreshold" pour définir une taille de fichier .ttf, en octets.
 // Si une police exportée crée un fichier d'une taille supérieure à celle-ci, alors l'opération de sauvegarde appliquera un sous-ensemble à cette police.
// La définition d'un seuil de 0 applique un sous-ensemble à toutes les polices,
// et le définir sur "int.MaxValue" désactive efficacement le sous-ensemble.
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
    // Par défaut, les fichiers .ttf de chacune de nos trois polices feront plus de 700 Mo.
    // Le sous-ensemble les réduira tous à moins de 30 Mo.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


