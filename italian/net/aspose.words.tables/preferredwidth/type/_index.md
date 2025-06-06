---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri la proprietà PreferredWidth Type, che definisce l'unità di misura per i valori di larghezza preferiti, migliorando la precisione e la flessibilità della progettazione.
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

Mostra come verificare il tipo di larghezza preferito e il valore di una cella di una tabella.

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
