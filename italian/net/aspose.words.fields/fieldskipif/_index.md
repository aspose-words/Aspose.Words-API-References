---
title: Class FieldSkipIf
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.FieldSkipIf classe. Implementa il campo SKIPIF.
type: docs
weight: 2420
url: /it/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

Implementa il campo SKIPIF.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldSkipIf : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldSkipIf](fieldskipif/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldskipif/comparisonoperator/) { get; set; } | Ottiene o imposta l'operatore di confronto. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non deve ricalcolare il risultato). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | Ottiene o imposta la parte sinistra dell'espressione di confronto. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | Ottiene o imposta la parte destra dell'espressione di confronto. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`nullo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo compreso tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi secondari. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce`nullo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un risultato se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Esegue un aggiornamento del campo. Genera un risultato se il campo è già in fase di aggiornamento. |

### Osservazioni

Confronta i valori designati dalle espressioni[`LeftExpression`](./leftexpression/) E[`RightExpression`](./rightexpression/) in confronto utilizzando l'operatore designato da[`ComparisonOperator`](./comparisonoperator/) . Se il confronto è vero, SKIPIF annulla il documento di unione corrente, passa al record di dati successivo nell'origine dati e avvia un nuovo documento di unione. Se il confronto è falso, il documento di unione corrente continua.

### Esempi

Mostra come saltare le pagine in una stampa unione utilizzando il campo SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un campo SKIPIF. Se la riga corrente di un'operazione di stampa unione soddisfa la condizione
// che indicano le espressioni di questo campo, l'operazione di stampa unione interrompe la riga corrente,
// elimina il documento di unione corrente, quindi passa immediatamente alla riga successiva per iniziare il documento di unione successivo.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Sposta il builder sul separatore del campo SKIPIF in modo da poter posizionare un MERGEFIELD all'interno del campo SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD si riferisce alla colonna "Dipartimento" nella nostra tabella dati. Se una riga da quella tabella
// ha il valore "HR" nella colonna "Dipartimento", questa riga soddisferà la condizione.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Aggiungi contenuto al nostro documento, crea l'origine dati ed esegui la stampa unione.
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

Mostra come utilizzare i campi MERGEREC e MERGESEQ per il numero e il conteggio dei record di stampa unione nei documenti di output di una stampa unione.

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

// Un campo MERGESEQ conterà il numero di unioni riuscite e stamperà il valore corrente su ciascuna rispettiva pagina.
// Se una stampa unione non salta alcuna riga e non richiama alcun campo SKIP/SKIPIF/NEXT/NEXTIF, tutte le unioni hanno esito positivo.
// I campi MERGESEQ e MERGEREC visualizzeranno gli stessi risultati della stampa unione riuscita.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Inserisci un campo SKIPIF, che salterà un'unione se il nome è "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Crea un'origine dati con 3 righe, una delle quali ha "John Doe" come valore per la colonna "Nome".
// Poiché un campo SKIPIF verrà attivato una volta da quel valore, l'output della nostra stampa unione avrà 2 pagine invece di 3.
// Nella pagina 1, i campi MERGESEQ e MERGEREC visualizzeranno entrambi "1".
// A pagina 2, il campo MERGEREC visualizzerà "3" e il campo MERGESEQ visualizzerà "2".
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);            
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


