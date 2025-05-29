---
title: FieldDate Class
linktitle: FieldDate
articleTitle: FieldDate
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldDate, progettata per implementare senza sforzo i campi DATA, migliorando l'automazione e la formattazione dei documenti.
type: docs
weight: 2180
url: /it/net/aspose.words.fields/fielddate/
---
## FieldDate class

Implementa il campo DATA.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldDate : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldDate](fielddate/)() | Default_Costruttore |

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
| [UseLastFormat](../../aspose.words.fields/fielddate/uselastformat/) { get; set; } | Ottiene o imposta se utilizzare un formato utilizzato per ultimo dall'applicazione di hosting quando si inserisce un nuovo campo DATA. |
| [UseLunarCalendar](../../aspose.words.fields/fielddate/uselunarcalendar/) { get; set; } | Ottiene o imposta se utilizzare il calendario lunare Hijri o quello ebraico. |
| [UseSakaEraCalendar](../../aspose.words.fields/fielddate/usesakaeracalendar/) { get; set; } | Ottiene o imposta se utilizzare il calendario dell'era Saka. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fielddate/useumalquracalendar/) { get; set; } | Ottiene o imposta se utilizzare il calendario Um-al-Qura. |

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

Inserisce la data e l'ora correnti. Per impostazione predefinita, viene utilizzato il calendario gregoriano.

## Esempi

Mostra come utilizzare i campi DATA per visualizzare le date in base a diversi tipi di calendari.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se vogliamo che il testo del documento visualizzi sempre la data corretta, possiamo utilizzare un campo DATA.
// Di seguito sono riportati tre tipi di calendari culturali che un campo DATA può utilizzare per visualizzare una data.
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

// Inserire un campo DATA e impostare il suo tipo di calendario su quello utilizzato per ultimo dall'applicazione host.
// In Microsoft Word, il tipo sarà quello utilizzato più di recente nella finestra di dialogo Inserisci -> Testo -> Data e ora.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
