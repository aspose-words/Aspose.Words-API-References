---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: Aspose.Words pour .NET
description: Découvrez comment l'énumération Aspose.Words XlsxSectionMode optimise l'enregistrement des documents au format XLSX, améliorant ainsi votre flux de travail et votre gestion des documents.
type: docs
weight: 6530
url: /fr/net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

Spécifie comment les sections sont gérées lors de l'enregistrement d'un document au format XLSX.

```csharp
public enum XlsxSectionMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| MultipleWorksheets | `0` | Spécifie qu'une feuille de calcul distincte est créée pour chaque section d'un document. |
| SingleWorksheet | `1` | Spécifie que toutes les sections d'un document sont enregistrées sur une seule feuille de calcul. |

## Exemples

Montre comment enregistrer un document sous forme de feuille de calcul distincte.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Chaque section d'un document sera créée comme une feuille de calcul distincte.
// Utilisez « SingleWorksheet » pour afficher tous les documents sur une seule feuille de calcul.
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
