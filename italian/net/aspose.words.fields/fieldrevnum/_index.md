---
title: FieldRevNum Class
linktitle: FieldRevNum
articleTitle: FieldRevNum
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldRevNum per un'implementazione fluida dei campi REVNUM. Migliora l'automazione dei documenti e semplifica l'efficienza del flusso di lavoro!
type: docs
weight: 2750
url: /it/net/aspose.words.fields/fieldrevnum/
---
## FieldRevNum class

Implementa il campo REVNUM.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldRevNum : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldRevNum](fieldrevnum/)() | Default_Costruttore |

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

Recupera il numero di revisione del documento, come registrato nel**Revisione** proprietà delle proprietà del documento incorporato .

## Esempi

Mostra come lavorare con i campi REVNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Current revision #");

// Inserire un campo REVNUM, che visualizza la proprietà del numero di revisione corrente del documento.
FieldRevNum field = (FieldRevNum)builder.InsertField(FieldType.FieldRevisionNum, true);

Assert.AreEqual(" REVNUM ", field.GetFieldCode());
Assert.AreEqual("1", field.Result);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.RevisionNumber);

// Questa proprietà conta quante volte un documento è stato salvato in Microsoft Word,
// e non è correlato alle revisioni tracciate. Possiamo trovarlo cliccando con il pulsante destro del mouse sul documento in Esplora risorse.
// tramite Proprietà -> Dettagli. Possiamo aggiornare questa proprietà manualmente.
doc.BuiltInDocumentProperties.RevisionNumber++;
field.Update();

Assert.AreEqual("2", field.Result);
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
