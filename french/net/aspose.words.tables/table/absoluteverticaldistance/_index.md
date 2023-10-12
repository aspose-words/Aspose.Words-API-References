---
title: Table.AbsoluteVerticalDistance
second_title: Référence de l'API Aspose.Words pour .NET
description: Table propriété. Obtient ou définit la position verticale absolue de la table flottante spécifiée par les propriétés de la table en points. La valeur par défaut est 0.
type: docs
weight: 30
url: /fr/net/aspose.words.tables/table/absoluteverticaldistance/
---
## Table.AbsoluteVerticalDistance property

Obtient ou définit la position verticale absolue de la table flottante spécifiée par les propriétés de la table, en points. La valeur par défaut est 0.

```csharp
public double AbsoluteVerticalDistance { get; set; }
```

### Exemples

Montre comment définir l'emplacement des tables flottantes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Définit l'emplacement du tableau à un endroit de la page, comme, dans ce cas, le coin inférieur droit.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Nous pouvons également définir un décalage horizontal et vertical en points par rapport à l'emplacement du paragraphe où nous avons inséré le tableau.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../table/)
* Assemblée [Aspose.Words](../../../)


