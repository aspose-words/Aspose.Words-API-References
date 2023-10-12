---
title: Class FieldMergeField
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.FieldMergeField classe. Implementa il campo MERGEFIELD.
type: docs
weight: 2150
url: /it/net/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class

Implementa il campo MERGEFIELD.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldMergeField : Field
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [FieldName](../../aspose.words.fields/fieldmergefield/fieldname/) { get; set; } | Ottiene o imposta il nome di un campo dati. |
| [FieldNameNoPrefix](../../aspose.words.fields/fieldmergefield/fieldnamenoprefix/) { get; } | Restituisce solo il nome del campo dati. Qualsiasi prefisso viene rimosso dalla proprietà prefisso. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non deve ricalcolare il risultato). |
| [IsMapped](../../aspose.words.fields/fieldmergefield/ismapped/) { get; set; } | Ottiene o imposta se questo campo è un campo mappato. |
| [IsVerticalFormatting](../../aspose.words.fields/fieldmergefield/isverticalformatting/) { get; set; } | Ottiene o imposta se abilitare la conversione dei caratteri per la formattazione verticale. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`nullo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [TextAfter](../../aspose.words.fields/fieldmergefield/textafter/) { get; set; } | Ottiene o imposta il testo da inserire dopo il campo se il campo non è vuoto. |
| [TextBefore](../../aspose.words.fields/fieldmergefield/textbefore/) { get; set; } | Ottiene o imposta il testo da inserire prima del campo se il campo non è vuoto. |
| override [Type](../../aspose.words.fields/fieldmergefield/type/) { get; } | Ottiene il tipo di campo Microsoft Word. |

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

Recupera il nome di un campo dati all'interno dei caratteri di unione in un documento principale di stampa unione. Quando il documento principale viene unito con l'origine dati selezionata, le informazioni dal campo dati specificato vengono inserite al posto del campo di unione.

### Esempi

Mostra come utilizzare i campi MERGEFIELD per eseguire una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabella dati da utilizzare come origine dati di stampa unione.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Inserisci un MERGEFIELD con una proprietà FieldName impostata sul nome di una colonna nell'origine dati.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Possiamo applicare del testo prima e dopo il valore accettato da questo campo quando avviene la fusione.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

// Inserisci un altro MERGEFIELD per una colonna diversa nell'origine dati.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


