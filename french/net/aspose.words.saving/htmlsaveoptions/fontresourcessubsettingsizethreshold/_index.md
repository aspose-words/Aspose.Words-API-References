---
title: FontResourcesSubsettingSizeThreshold
second_title: Référence de l'API Aspose.Words pour .NET
description: Contrôle les ressources de police qui nécessitent un sousensemble lors de lenregistrement au format HTML MHTML ou EPUB. La valeur par défaut est0 .
type: docs
weight: 300
url: /fr/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Contrôle les ressources de police qui nécessitent un sous-ensemble lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### Remarques

[`ExportFontResources`](../exportfontresources/) permet d'exporter des polices en tant que fichiers subsidiaires ou en tant que parties du package output . Si le document utilise de nombreuses polices, en particulier avec un grand nombre de glyphes, la taille de sortie peut augmenter de manière significative . Le sous-ensemble de police réduit la taille de la ressource de police exportée en filtrant les glyphes qui ne sont pas utilisés par le document actuel.

Le sous-ensemble de polices fonctionne comme suit :

* Par défaut, toutes les polices exportées sont des sous-ensembles.
* Paramètre`FontResourcesSubsettingSizeThreshold`à une valeur positive indique à Aspose.Words de créer un sous-ensemble de polices dont la taille de fichier est supérieure à la valeur spécifiée.
* Définition de la propriété surMaxValue supprime les sous-ensembles de polices.

**Important!** Lors de l'exportation de ressources de polices, les problèmes de licence de police doivent être pris en compte. Les auteurs qui souhaitent utiliser des polices spécifiques via un mécanisme de police téléchargeable doivent toujours vérifier soigneusement que leur utilisation prévue est dans le cadre de la licence de police. De nombreuses polices commerciales n'autorisent pas actuellement le téléchargement Web de leurs polices sous quelque forme que ce soit. Les accords de licence qui couvrent certaines polices précisent spécifiquement que l'utilisation via **@fontface** rules dans les feuilles de style CSS n'est pas autorisé. Les sous-ensembles de polices peuvent également enfreindre les termes de la licence.

### Exemples

Montre comment travailler avec des sous-ensembles de polices.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un sous-ensemble de police de configuration de l'objet SaveOptions.
// Supposons que nous définissions le drapeau "ExportFontResources" sur "true" et que nous nommions également un dossier dans la propriété "FontsFolder".
// Dans ce cas, l'opération de sauvegarde créera ce dossier et placera un fichier .ttf à l'intérieur
// ce dossier pour chaque police utilisée par notre document.
// Chaque fichier .ttf contiendra le jeu de glyphes complet de cette police,
// ce qui peut potentiellement entraîner un fichier très volumineux qui accompagne le document.
// Lorsque nous appliquons un sous-ensemble à une police, ses données brutes exportées ne contiendront que les glyphes du document
// utilisant à la place du jeu de glyphes entier. Si le texte de notre document n'utilise qu'une petite fraction de la police
// jeu de glyphes, alors le sous-ensemble réduira considérablement la taille de nos documents de sortie.
// On peut utiliser la propriété "FontResourcesSubsettingSizeThreshold" pour définir une taille de fichier .ttf, en octets.
 // Si une police exportée crée un fichier de taille supérieure à celle-ci, l'opération de sauvegarde appliquera un sous-ensemble à cette police.
// La définition d'un seuil de 0 applique le sous-ensemble à toutes les polices,
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
    // Par défaut, les fichiers .ttf pour chacune de nos trois polices feront plus de 700 Mo.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
