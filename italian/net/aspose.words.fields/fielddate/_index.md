---
title: FieldDate
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo DATA.
type: docs
weight: 1620
url: /it/net/aspose.words.fields/fielddate/
---
## FieldDate class

Implementa il campo DATA.

```csharp
public class FieldDate : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldDate](fielddate)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ottiene il tipo di campo di Microsoft Word. |
| [UseLastFormat](../../aspose.words.fields/fielddate/uselastformat) { get; set; } | Ottiene o imposta se utilizzare un formato utilizzato per ultimo dall'applicazione di hosting quando si inserisce un nuovo campo DATE. |
| [UseLunarCalendar](../../aspose.words.fields/fielddate/uselunarcalendar) { get; set; } | Ottiene o imposta se utilizzare il calendario lunare Hijri o il calendario lunare ebraico. |
| [UseSakaEraCalendar](../../aspose.words.fields/fielddate/usesakaeracalendar) { get; set; } | Ottiene o imposta se utilizzare il calendario dell'era Saka. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fielddate/useumalquracalendar) { get; set; } | Ottiene o imposta se utilizzare il calendario Um-al-Qura. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Inserisce la data e l'ora correnti. Per impostazione predefinita, viene utilizzato il calendario gregoriano.

### Esempi

Mostra come utilizzare i campi DATA per visualizzare le date in base a diversi tipi di calendari.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se vogliamo che il testo nel documento visualizzi sempre la data corretta, possiamo usare un campo DATA.
// Di seguito sono riportati tre tipi di calendari culturali che un campo DATE può utilizzare per visualizzare una data.
// 1 - Calendario lunare islamico:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Calendario di Umm al-Qura:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Calendario nazionale indiano:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Inserisci un campo DATA e imposta il tipo di calendario su quello utilizzato per ultimo dall'applicazione host.
// In Microsoft Word, il tipo sarà quello utilizzato più di recente in Inserisci -> Testo -> Finestra di dialogo Data e ora.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
