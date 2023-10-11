---
title: PclSaveOptions.FallbackFontName
second_title: Référence de l'API Aspose.Words pour .NET
description: PclSaveOptions propriété. Nom de la police qui sera utilisée si aucune police attendue nest trouvée dans les collections de polices dimprimante et intégrées.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Nom de la police qui sera utilisée si aucune police attendue n'est trouvée dans les collections de polices d'imprimante et intégrées.

```csharp
public string FallbackFontName { get; set; }
```

### Remarques

Si aucune solution de secours n'est trouvée, un avertissement est généré et la police "Arial" est utilisée.

### Exemples

Montre comment déclarer une police qu'une imprimante appliquera au texte imprimé en remplacement si sa police d'origine n'est pas disponible.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Ce document demandera à l'imprimeur d'appliquer "Times New Roman" au texte avec la police manquante.
// Si "Times New Roman" n'est également pas disponible, l'imprimante utilisera par défaut la police "Arial".
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Voir également

* class [PclSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pclsaveoptions/)
* Assemblée [Aspose.Words](../../../)


