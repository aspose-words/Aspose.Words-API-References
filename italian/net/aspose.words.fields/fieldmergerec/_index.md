---
title: FieldMergeRec Class
linktitle: FieldMergeRec
articleTitle: FieldMergeRec
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldMergeRec per unire i documenti in modo fluido con il campo MERGEREC. Migliora l'automazione dei tuoi documenti oggi stesso!
type: docs
weight: 2570
url: /it/net/aspose.words.fields/fieldmergerec/
---
## FieldMergeRec class

Implementa il campo MERGEREC.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldMergeRec : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldMergeRec](fieldmergerec/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo nodo figlio del suo nodo padre, restituisce il paragrafo padre. Se il campo è già stato rimosso, restituisce`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Esegue un aggiornamento di campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |

## Osservazioni

Al momento i campi MERGEREC e MERGESEQ implementano la stessa funzionalità perché non sappiamo con certezza come ignorare i record nella stampa unione di Aspose.Words.

## Esempi

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

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
