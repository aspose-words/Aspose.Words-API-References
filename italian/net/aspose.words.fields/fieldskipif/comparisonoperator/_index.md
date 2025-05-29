---
title: FieldSkipIf.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldSkipIf ComparisonOperator, gestisci e personalizza facilmente i tuoi operatori di confronto per una migliore gestione dei dati.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldskipif/comparisonoperator/
---
## FieldSkipIf.ComparisonOperator property

Ottiene o imposta l'operatore di confronto.

```csharp
public string ComparisonOperator { get; set; }
```

## Esempi

Mostra come saltare le pagine in una stampa unione utilizzando il campo SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un campo SKIPIF. Se la riga corrente di un'operazione di stampa unione soddisfa la condizione
// se le espressioni di questo campo indicano, l'operazione di unione di posta interrompe la riga corrente,
// scarta il documento di unione corrente e passa immediatamente alla riga successiva per iniziare il documento di unione successivo.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Spostiamo il builder sul separatore del campo SKIPIF in modo da poter posizionare un MERGEFIELD all'interno del campo SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// Il MERGEFIELD si riferisce alla colonna "Dipartimento" nella nostra tabella dati. Se una riga di quella tabella
// ha un valore di "HR" nella sua colonna "Department", allora questa riga soddisferà la condizione.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Aggiungiamo contenuto al nostro documento, creiamo l'origine dati ed eseguiamo la stampa unione.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // Questa tabella ha tre righe e una di queste soddisfa la condizione del nostro campo SKIPIF.
// La stampa unione produrrà due pagine.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Mostra come utilizzare i campi MERGEREC e MERGESEQ per numerare e contare i record di stampa unione nei documenti di output di una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Un campo MERGEREC stamperà il numero di riga dei dati da unire in ogni documento di output dell'unione.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Un campo MERGESEQ conterà il numero di unioni riuscite e stamperà il valore corrente su ogni pagina corrispondente.
// Se una stampa unione non salta alcuna riga e non richiama alcun campo SKIP/SKIPIF/NEXT/NEXTIF, tutte le unioni avranno esito positivo.
// I campi MERGESEQ e MERGEREC visualizzeranno gli stessi risultati se la loro unione dati ha avuto esito positivo.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Inserire un campo SKIPIF, che salterà l'unione se il nome è "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Crea un'origine dati con 3 righe, una delle quali con "John Doe" come valore per la colonna "Nome".
// Poiché un campo SKIPIF verrà attivato una volta da quel valore, l'output della nostra stampa unione avrà 2 pagine anziché 3.
// A pagina 1, i campi MERGESEQ e MERGEREC visualizzeranno entrambi "1".
// A pagina 2, il campo MERGEREC visualizzerà "3" e il campo MERGESEQ visualizzerà "2".
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add("Jane Doe");
table.Rows.Add("John Doe");
table.Rows.Add("Joe Bloggs");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Guarda anche

* class [FieldSkipIf](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
