---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Table AllowAutoFit pour redimensionner sans effort les cellules des tableaux Microsoft Word et Aspose.Words, améliorant ainsi la lisibilité et la présentation de votre document.
type: docs
weight: 50
url: /fr/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Permet à Microsoft Word et Aspose.Words de redimensionner automatiquement les cellules d'un tableau pour les adapter à leur contenu.

```csharp
public bool AllowAutoFit { get; set; }
```

## Remarques

La valeur par défaut est`vrai`.

## Exemples

Montre comment activer/désactiver le redimensionnement automatique des cellules du tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// Définissez la propriété « AllowAutoFit » sur « false » pour que le tableau conserve les dimensions
// de toutes ses lignes et cellules, et tronque le contenu s'il devient trop grand pour tenir.
// Définissez la propriété « AllowAutoFit » sur « true » pour permettre au tableau de modifier la largeur et la hauteur de ses cellules
// pour accueillir leur contenu.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
