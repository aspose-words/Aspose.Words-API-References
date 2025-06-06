---
title: ConditionalStyle.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words per .NET
description: Formattazione chiara e senza sforzo con il metodo ClearFormatting di ConditionalStyle. Semplifica il tuo processo di progettazione e migliora la chiarezza dei documenti oggi stesso!
type: docs
weight: 100
url: /it/net/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle.ClearFormatting method

Cancella la formattazione di questo stile condizionale.

```csharp
public void ClearFormatting()
```

## Esempi

Mostra come reimpostare gli stili condizionali delle tabelle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("First row");
builder.EndRow();
builder.InsertCell();
builder.Write("Last row");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
table.Style = tableStyle;

// Imposta lo stile della tabella per colorare in rosso i bordi della prima riga della tabella.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Imposta lo stile della tabella per colorare in blu i bordi dell'ultima riga della tabella.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Di seguito sono riportati due modi per utilizzare il metodo "ClearFormatting" per cancellare gli stili condizionali.
// 1 - Cancella gli stili condizionali per una parte specifica di una tabella:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Cancella gli stili condizionali per l'intera tabella:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Guarda anche

* class [ConditionalStyle](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
