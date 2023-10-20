---
title: Story.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words per .NET
description: Story Tables proprietà. Ottiene una raccolta di tabelle che sono figli immediati della storia in C#.
type: docs
weight: 50
url: /it/net/aspose.words/story/tables/
---
## Story.Tables property

Ottiene una raccolta di tabelle che sono figli immediati della storia.

```csharp
public TableCollection Tables { get; }
```

## Esempi

Mostra come rimuovere la prima e l'ultima riga di tutte le tabelle in un documento.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

### Guarda anche

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [Story](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
