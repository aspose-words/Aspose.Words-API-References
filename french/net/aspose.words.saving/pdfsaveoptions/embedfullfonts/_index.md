---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words pour .NET
description: Découvrez comment la fonctionnalité PdfSaveOptions EmbedFullFonts améliore vos documents PDF en garantissant une intégration complète des polices pour une mise en forme parfaite.
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

La valeur par défaut est`FAUX`, ce qui signifie que les polices sont sous-ensembleées avant l'incorporation. Le sous-ensemble est utile si vous souhaitez réduire la taille du fichier de sortie. Le sous-ensemble supprime tous les glyphes inutilisés d'une police.

Lorsque cette valeur est définie sur`vrai`Un fichier de police complet est intégré au PDF sans sous-ensemble. Cela génère des fichiers de sortie plus volumineux, mais peut s'avérer utile si vous souhaitez modifier ultérieurement le PDF obtenu (par exemple, ajouter du texte).

Certaines polices sont volumineuses (plusieurs mégaoctets) et leur intégration sans subsetting entraînera des documents de sortie volumineux.

## Exemples

Montre comment activer ou désactiver le sous-ensemble lors de l'incorporation de polices lors du rendu d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Configurez nos sources de polices pour garantir que nous avons accès aux deux polices de ce document.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Étant donné que notre document contient une police personnalisée, son intégration dans le document de sortie peut être souhaitable.
// Définissez la propriété « EmbedFullFonts » sur « true » pour intégrer chaque glyphe de chaque police intégrée dans le PDF de sortie.
// La taille du document peut devenir très grande, mais nous aurons pleinement accès à toutes les polices si nous éditons le PDF.
// Définissez la propriété « EmbedFullFonts » sur « false » pour appliquer un sous-ensemble aux polices, en enregistrant uniquement les glyphes
// que le document utilise. Le fichier sera considérablement plus petit,
// mais nous pouvons avoir besoin d'accéder à des polices personnalisées si nous modifions le document.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

// Restaurer les sources de polices d'origine.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
