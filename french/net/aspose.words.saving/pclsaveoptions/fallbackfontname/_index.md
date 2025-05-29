---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PclSaveOptions FallbackFontName, qui garantit une impression transparente avec une police par défaut lorsque la police souhaitée n'est pas disponible.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Nom de la police qui sera utilisée si aucune police attendue n'est trouvée dans l'imprimante et les collections de polices intégrées.

```csharp
public string FallbackFontName { get; set; }
```

## Remarques

Si aucune solution de secours n'est trouvée, un avertissement est généré et la police « Arial » est utilisée.

## Exemples

Montre comment déclarer une police qu'une imprimante appliquera au texte imprimé en remplacement si sa police d'origine n'est pas disponible.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Ce document demandera à l'imprimante d'appliquer « Times New Roman » au texte avec la police manquante.
// Si « Times New Roman » n'est pas disponible, l'imprimante utilisera par défaut la police « Arial ».
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Voir également

* class [PclSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
