---
title: CellFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words per .NET
description: Scopri la proprietà CellFormat Borders per accedere e personalizzare le raccolte di bordi delle celle, per migliorare la progettazione e le funzionalità del foglio di calcolo.
type: docs
weight: 10
url: /it/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

Ottiene la raccolta dei bordi della cella.

```csharp
public BorderCollection Borders { get; }
```

## Esempi

Mostra come combinare le righe di due tabelle in una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 - Dalla raccolta "Tabelle" di un nodo Corpo:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilizzo del metodo "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Aggiunge tutte le righe dalla tabella corrente a quella successiva.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Rimuove il contenitore della tabella vuota.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Guarda anche

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
