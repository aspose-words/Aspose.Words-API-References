---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words pour .NET
description: PdfSaveOptions EmbedFullFonts propriété. Contrôle la manière dont les polices sont intégrées dans les documents PDF résultants en C#.
type: docs
weight: 120
url: /fr/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

Contrôle la manière dont les polices sont intégrées dans les documents PDF résultants.

```csharp
public bool EmbedFullFonts { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`, ce qui signifie que les polices sont divisées en sous-ensembles avant l'intégration. Le sous-ensemble est utile si vous souhaitez réduire la taille du fichier de sortie. Le sous-ensemble supprime tous les glyphes inutilisés all d'une police.

Lorsque cette valeur est fixée à`vrai`, un fichier de police complet est intégré dans le PDF sans sous-ensemble . Cela entraînera des fichiers de sortie plus volumineux, mais peut être une option utile lorsque vous souhaitez modifier le PDF résultant ultérieurement (par exemple, ajouter plus de texte).

Certaines polices sont volumineuses (plusieurs mégaoctets) et leur intégration sans subsetting entraînera des documents de sortie volumineux.

## Exemples

Montre comment activer ou désactiver les sous-paramètres lors de l'intégration de polices lors du rendu d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Configurez nos sources de polices pour nous assurer que nous avons accès aux deux polices de ce document.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource = new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Puisque notre document contient une police personnalisée, l'intégration dans le document de sortie peut être souhaitable.
// Définissez la propriété "EmbedFullFonts" sur "true" pour intégrer chaque glyphe de chaque police incorporée dans le PDF de sortie.
// La taille du document peut devenir très grande, mais nous aurons pleinement accès à toutes les polices si nous éditons le PDF.
// Définissez la propriété "EmbedFullFonts" sur "false" pour appliquer un sous-ensemble aux polices, en enregistrant uniquement les glyphes
// que le document utilise. Le fichier sera considérablement plus petit,
// mais nous pourrions avoir besoin d'accéder à des polices personnalisées si nous modifions le document.
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
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
