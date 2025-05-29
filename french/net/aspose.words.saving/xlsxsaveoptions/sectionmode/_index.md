---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SectionMode XlsxSaveOptions optimise la gestion des sections pour les exportations XLSX, garantissant une gestion transparente des documents et plusieurs feuilles de calcul.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

Obtient ou définit la manière dont les sections sont gérées lors de l'enregistrement dans le document XLSX de sortie. La valeur par défaut estMultipleWorksheets .

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

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

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
