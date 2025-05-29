---
title: Table.RelativeVerticalAlignment
linktitle: RelativeVerticalAlignment
articleTitle: RelativeVerticalAlignment
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Table RelativeVerticalAlignment pour gérer facilement l'alignement vertical des tableaux flottants, améliorant ainsi la précision et la conception de votre mise en page.
type: docs
weight: 240
url: /fr/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

Obtient ou définit l'alignement vertical relatif de la table flottante.

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
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

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
