---
title: PdfSaveOptions.PdfSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions constructeur. Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans the Pdf format.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans the Pdf format.

```csharp
public PdfSaveOptions()
```

### Exemples

Montre comment activer ou désactiver les sous-ensembles lors de l'incorporation de polices lors du rendu d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Configurez nos sources de polices pour vous assurer que nous avons accès aux deux polices de ce document.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource = new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Étant donné que notre document contient une police personnalisée, l'intégration dans le document de sortie peut être souhaitable.
// Définissez la propriété "EmbedFullFonts" sur "true" pour incorporer chaque glyphe de chaque police incorporée dans le PDF de sortie.
// La taille du document peut devenir très grande, mais nous aurons pleinement accès à toutes les polices si nous modifions le PDF.
// Définissez la propriété "EmbedFullFonts" sur "false" pour appliquer un sous-ensemble aux polices, en enregistrant uniquement les glyphes
// que le document utilise. Le fichier sera considérablement plus petit,
// mais nous aurons peut-être besoin d'accéder à des polices personnalisées si nous modifions le document.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

if (embedFullFonts)
    Assert.That(500000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));
else
    Assert.That(25000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));

// Restaure les sources de polices d'origine.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


