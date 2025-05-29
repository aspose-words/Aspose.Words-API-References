---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Range, la chiave per gestire le sezioni dei documenti senza sforzo. Migliora l'elaborazione dei tuoi documenti con controllo e flessibilità impeccabili.
type: docs
weight: 5250
url: /it/net/aspose.words/range/
---
## Range class

Rappresenta un'area contigua in un documento.

Per saperne di più, visita il[Lavorare con gli intervalli](https://docs.aspose.com/words/net/working-with-ranges/) articolo di documentazione.

```csharp
public class Range : IEnumerable<Node>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Restituisce un[`Bookmarks`](./bookmarks/) raccolta che rappresenta tutti i segnalibri nell'intervallo. |
| [Fields](../../aspose.words/range/fields/) { get; } | Restituisce un[`Fields`](./fields/) raccolta che rappresenta tutti i campi nell'intervallo. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Restituisce un[`FormFields`](./formfields/) raccolta che rappresenta tutti i campi del modulo nell'intervallo. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Ottiene una raccolta di revisioni (modifiche tracciate) presenti in questo intervallo. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Restituisce un[`StructuredDocumentTags`](./structureddocumenttags/) raccolta che rappresenta tutti i tag di documenti strutturati nell'intervallo. |
| [Text](../../aspose.words/range/text/) { get; } | Ottiene il testo dell'intervallo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Elimina tutti i caratteri dell'intervallo. |
| [GetEnumerator](../../aspose.words/range/getenumerator/)() |  |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Modifica i valori del tipo di campo[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) Di[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) in questo intervallo in modo che corrispondano ai tipi di campo contenuti nei codici di campo. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | Sostituisce tutte le occorrenze di un pattern di caratteri specificato da un'espressione regolare con un'altra stringa. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa sostitutiva. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Sostituisce tutte le occorrenze di un pattern di caratteri specificato da un'espressione regolare con un'altra stringa. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa sostitutiva. |
| [ToDocument](../../aspose.words/range/todocument/)() | Crea un nuovo documento completamente formato che contiene l'intervallo. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Scollega i campi in questo intervallo. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Aggiorna i valori dei campi del documento in questo intervallo. |

## Osservazioni

Il documento è rappresentato da un albero di nodi e i nodi forniscono operations per lavorare con l'albero, ma alcune operazioni sono più facili da eseguire se document viene trattato come una sequenza contigua di testo.

`Range` è un'interfaccia "facciata" che fornisce metodi che trattano document o parti del documento come testo "piatto", indipendentemente dal fatto che i nodi document siano memorizzati in un modello di oggetti ad albero.

`Range` non contiene testo o nodi, è semplicemente una vista o "finestra" su un frammento di un documento.

## Esempi

Mostra come ottenere il contenuto testuale di tutti i nodi compresi in un intervallo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Guarda anche

* class [Node](../node/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
