---
title: FieldGreetingLine
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo GREETINGLINE.
type: docs
weight: 1830
url: /it/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

Implementa il campo GREETINGLINE.

```csharp
public class FieldGreetingLine : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldGreetingLine](fieldgreetingline)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext) { get; set; } | Ottiene o imposta il testo da includere nel campo se il nome è vuoto. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid) { get; set; } | Ottiene o imposta l'id della lingua utilizzato per formattare il nome. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat) { get; set; } | Ottiene o imposta il formato del nome incluso nel campo. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames)() | Restituisce una raccolta di nomi di campi stampa unione utilizzati dal campo. |
| [Remove](../../aspose.words.fields/field/remove)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Inserisce una riga di saluto per la stampa unione.

### Esempi

Mostra come inserire un campo GREETINGLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un saluto generico utilizzando un campo GREETINGLINE e del testo dopo di esso.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Un campo GREETINGLINE accetta valori da un'origine dati durante una stampa unione, come un MERGEFIELD.
// Può anche formattare il modo in cui i dati dell'origine vengono scritti al suo posto una volta completata la stampa unione.
// La raccolta dei nomi dei campi corrisponde alle colonne dell'origine dati
// da cui il campo prenderà i valori.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Per popolare quell'array, dobbiamo specificare un formato per la nostra linea di saluto.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Ora, il nostro campo accetterà i valori di queste due colonne nell'origine dati.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Questa stringa coprirà tutti i casi in cui i dati della tabella di dati non sono validi
// sostituendo il nome non corretto con una stringa.
field.AlternateText = "Sir or Madam";

// Imposta una lingua per formattare il risultato.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Crea una tabella di dati con colonne i cui nomi corrispondono agli elementi
// dalla raccolta dei nomi dei campi del campo, quindi eseguire la stampa unione.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Questa riga ha un valore non valido nella colonna del titolo di cortesia, quindi il nostro saluto verrà impostato automaticamente sul testo alternativo.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields, Is.Empty);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
