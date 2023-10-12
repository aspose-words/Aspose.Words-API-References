---
title: Table.AllowCellSpacing
second_title: Référence de l'API Aspose.Words pour .NET
description: Table propriété. Obtient ou définit loption  Autoriser lespacement entre les cellules .
type: docs
weight: 60
url: /fr/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

Obtient ou définit l'option « Autoriser l'espacement entre les cellules ».

```csharp
public bool AllowCellSpacing { get; set; }
```

### Exemples

Montre comment activer l’espacement entre les cellules individuelles d’un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Définissez la propriété "AllowCellSpacing" sur "true" pour activer l'espacement entre les cellules
// d'une grandeur égale à la valeur de la propriété "CellSpacing", en points.
// Définissez la propriété "AllowCellSpacing" sur "false" pour désactiver l'espacement des cellules
// et ignore la valeur de la propriété "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// L'ajustement de la propriété "CellSpacing" activera automatiquement l'espacement des cellules.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../table/)
* Assemblée [Aspose.Words](../../../)


