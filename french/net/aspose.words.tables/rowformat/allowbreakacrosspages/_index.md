---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words pour .NET
description: Découvrez la propriété RowFormat AllowBreakAcrossPages, activez un flux de texte transparent dans les lignes de tableau à travers les sauts de page pour une lisibilité et une présentation améliorées.
type: docs
weight: 10
url: /fr/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Vrai si le texte d'une ligne de tableau est autorisé à être divisé sur un saut de page.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Exemples

Montre comment désactiver la séparation des lignes sur plusieurs pages pour chaque ligne d'un tableau.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Définissez la propriété « AllowBreakAcrossPages » sur « false » pour conserver la ligne
// en un seul morceau si un tableau s'étend sur deux pages, qui se divisent le long de cette ligne.
// Si la ligne est trop grande pour tenir sur une page, Microsoft Word la repoussera vers la page suivante.
// Définissez la propriété « AllowBreakAcrossPages » sur « true » pour permettre à la ligne d'être divisée sur deux pages.
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Voir également

* class [RowFormat](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
