---
title: Table.AllowCellSpacing
linktitle: AllowCellSpacing
articleTitle: AllowCellSpacing
second_title: Aspose.Words per .NET
description: Table AllowCellSpacing proprietà. Ottiene o imposta lopzione Consenti spaziatura tra celle in C#.
type: docs
weight: 60
url: /it/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

Ottiene o imposta l'opzione "Consenti spaziatura tra celle".

```csharp
public bool AllowCellSpacing { get; set; }
```

## Esempi

Mostra come abilitare la spaziatura tra le singole celle in una tabella.

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

// Imposta la proprietà "AllowCellSpacing" su "true" per abilitare la spaziatura tra le celle
// con una grandezza pari al valore della proprietà "CellSpacing", in punti.
// Imposta la proprietà "AllowCellSpacing" su "false" per disabilitare la spaziatura delle celle
// e ignora il valore della proprietà "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// La regolazione della proprietà "CellSpacing" abiliterà automaticamente la spaziatura delle celle.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
