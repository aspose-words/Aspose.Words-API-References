---
title: FieldAuthor Class
linktitle: FieldAuthor
articleTitle: FieldAuthor
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldAuthor, progettata per implementare senza sforzo il campo AUTHOR per una migliore gestione e automazione dei documenti.
type: docs
weight: 1980
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

Recupera e, facoltativamente, imposta il nome dell'autore del documento, come registrato nel**Autore** proprietà delle proprietà del documento incorporato .

## Esempi

Mostra come utilizzare un campo AUTORE per visualizzare il nome del creatore di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I campi AUTHOR ricavano i risultati dalla proprietà del documento integrata denominata "Author".
// Se creiamo e salviamo un documento in Microsoft Word,
// conterrà il nostro nome utente in quella proprietà.
// Tuttavia, se creiamo un documento a livello di programmazione utilizzando Aspose.Words,
// la proprietà "Autore", per impostazione predefinita, sarà una stringa vuota.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Imposta un nome autore di backup per i campi AUTORE da utilizzare
// se la proprietà "Author" contiene una stringa vuota.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Aggiornamento di un campo AUTORE che contiene un valore
// applicherà quel valore alla proprietà incorporata "Author".
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Modificando questa proprietà e quindi aggiornando il campo AUTORE, questo valore verrà applicato al campo.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Se aggiorniamo un campo AUTORE dopo aver modificato la sua proprietà "Nome",
// quindi il campo visualizzerà il nuovo nome e applicherà il nuovo nome alla proprietà incorporata.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// I campi AUTHOR non influiscono sulla proprietà DefaultDocumentAuthor.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
