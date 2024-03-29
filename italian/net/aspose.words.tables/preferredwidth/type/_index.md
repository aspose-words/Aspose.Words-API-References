---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: PreferredWidth Type proprietà. Ottiene lunità di misura utilizzata per questo valore di larghezza preferito in C#.
type: docs
weight: 40
url: /it/net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

Ottiene l'unità di misura utilizzata per questo valore di larghezza preferito.

```csharp
public PreferredWidthType Type { get; }
```

## Esempi

Mostra come verificare il tipo di larghezza e il valore preferiti di una cella di tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Guarda anche

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
