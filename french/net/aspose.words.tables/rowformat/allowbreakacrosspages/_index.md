---
title: RowFormat.AllowBreakAcrossPages
second_title: Référence de l'API Aspose.Words pour .NET
description: RowFormat propriété. Vrai si le texte dune ligne de tableau est autorisé à être fractionné sur un saut de page.
type: docs
weight: 10
url: /fr/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Vrai si le texte d'une ligne de tableau est autorisé à être fractionné sur un saut de page.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

### Exemples

Montre comment désactiver les sauts de lignes sur plusieurs pages pour chaque ligne d'un tableau.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Définissez la propriété "AllowBreakAcrossPages" sur "false" pour conserver la ligne
// en un seul morceau si un tableau s'étend sur deux pages, qui se séparent le long de cette ligne.
// Si la ligne est trop grande pour tenir sur une page, Microsoft Word la poussera vers la page suivante.
// Définissez la propriété "AllowBreakAcrossPages" sur "true" pour permettre à la ligne de se répartir sur deux pages.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Voir également

* class [RowFormat](../)
* espace de noms [Aspose.Words.Tables](../../rowformat/)
* Assemblée [Aspose.Words](../../../)


