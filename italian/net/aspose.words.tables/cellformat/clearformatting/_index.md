---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words per .NET
description: Scopri il metodo ClearFormatting di CellFormat per ripristinare facilmente gli stili di cella predefiniti senza modificarne la larghezza. Migliora l'efficienza del tuo foglio di calcolo!
type: docs
weight: 160
url: /it/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Ripristina la formattazione predefinita della cella. Non modifica la larghezza della cella.

```csharp
public void ClearFormatting()
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

* class [CellFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
