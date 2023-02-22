---
title: Class FieldQuote
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.FieldQuote classe. Implementa il campo QUOTE.
type: docs
weight: 2160
url: /it/net/aspose.words.fields/fieldquote/
---
## FieldQuote class

Implementa il campo QUOTE.

```csharp
public class FieldQuote : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldQuote](fieldquote/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [Text](../../aspose.words.fields/fieldquote/text/) { get; set; } | Ottiene o imposta il testo da recuperare. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Recupera il testo specificato.

### Esempi

Mostra di utilizzare il campo PREVENTIVO.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un campo QUOTE, che visualizzerà il valore della sua proprietà Text.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Inserisci un campo QUOTE e nidifica un campo DATE al suo interno.
// I campi DATA aggiornano il loro valore alla data corrente ogni volta che apriamo il documento utilizzando Microsoft Word.
// Annidare il campo DATE all'interno del campo QUOTE in questo modo ne bloccherà il valore
// alla data in cui abbiamo creato il documento.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Aggiorna tutti i campi per visualizzare i risultati corretti.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


