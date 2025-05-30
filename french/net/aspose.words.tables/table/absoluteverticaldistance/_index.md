---
title: Table.AbsoluteVerticalDistance
linktitle: AbsoluteVerticalDistance
articleTitle: AbsoluteVerticalDistance
second_title: Aspose.Words pour .NET
description: Découvrez la propriété AbsoluteVerticalDistance pour les tableaux  contrôlez le positionnement vertical en points pour une mise en page précise. La valeur par défaut est 0. Optimisez votre conception !
type: docs
weight: 30
url: /fr/net/aspose.words.tables/table/absoluteverticaldistance/
---
## Table.AbsoluteVerticalDistance property

Obtient ou définit la position verticale absolue du tableau flottant spécifiée par les propriétés du tableau, en points. La valeur par défaut est 0.

```csharp
public double AbsoluteVerticalDistance { get; set; }
```

## Exemples

Montre comment définir l'emplacement des tables flottantes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Définissez l'emplacement du tableau sur un endroit de la page, comme, dans ce cas, le coin inférieur droit.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Nous pouvons également définir un décalage horizontal et vertical en points à partir de l'emplacement du paragraphe où nous avons inséré le tableau.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
