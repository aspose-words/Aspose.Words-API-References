---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: Aspose.Words pour .NET
description: SaveOptions ExportGeneratorName propriété. Quandvrai  entraîne lintégration du nom et de la version dAspose.Words dans les fichiers produits. La valeur par défaut estvrai  en C#.
type: docs
weight: 80
url: /fr/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

Quand`vrai` , entraîne l'intégration du nom et de la version d'Aspose.Words dans les fichiers produits. La valeur par défaut est`vrai` .

```csharp
public bool ExportGeneratorName { get; set; }
```

## Exemples

Montre comment désactiver l’ajout du nom et de la version d’Aspose.Words dans les fichiers produits.

```csharp
Document doc = new Document();

// Utilisez https://docs.aspose.com/words/net/generator-or-producer-name-inclus-in-output-documents/ pour savoir comment vérifier le résultat.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
