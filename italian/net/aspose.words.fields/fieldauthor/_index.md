---
title: Class FieldAuthor
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.FieldAuthor classe. Implementa il campo AUTORE.
type: docs
weight: 1570
url: /it/net/aspose.words.fields/fieldauthor/
---
## FieldAuthor class

Implementa il campo AUTORE.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldAuthor : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldAuthor](fieldauthor/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AuthorName](../../aspose.words.fields/fieldauthor/authorname/) { get; set; } | Ottiene o imposta il nome dell'autore del documento. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non deve ricalcolare il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
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

Recupera e facoltativamente imposta il nome dell'autore del documento, come registrato nel **Autore** proprietà delle proprietà del documento integrate.

### Esempi

Mostra come utilizzare un campo AUTORE per visualizzare il nome dell'autore del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I campi AUTORE ottengono i risultati dalla proprietà del documento incorporata chiamata "Autore".
// Se creiamo e salviamo un documento in Microsoft Word,
// avrà il nostro nome utente in quella proprietà.
// Tuttavia, se creiamo un documento a livello di codice utilizzando Aspose.Words,
// la proprietà "Autore", per impostazione predefinita, sarà una stringa vuota.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Imposta un nome autore di backup per i campi AUTHOR da utilizzare
// se la proprietà "Autore" contiene una stringa vuota.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Aggiornamento di un campo AUTHOR che contiene un valore
// applicherà quel valore alla proprietà incorporata "Autore".
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// La modifica di questa proprietà e l'aggiornamento del campo AUTORE applicheranno questo valore al campo.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Se aggiorniamo un campo AUTORE dopo aver modificato la sua proprietà "Nome",
// il campo visualizzerà il nuovo nome e applicherà il nuovo nome alla proprietà incorporata.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// I campi AUTORE non influiscono sulla proprietà DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


