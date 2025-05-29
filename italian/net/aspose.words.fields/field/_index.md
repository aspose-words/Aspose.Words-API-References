---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.Field, la chiave per migliorare i documenti Microsoft Word con campi dinamici per una maggiore funzionalità ed efficienza.
type: docs
weight: 1920
url: /it/net/aspose.words.fields/field/
---
## Field class

Rappresenta un campo del documento Microsoft Word.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class Field
```

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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo nodo figlio del suo nodo padre, restituisce il paragrafo padre. Se il campo è già stato rimosso, restituisce`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/#update)() | Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Esegue un aggiornamento di campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |

## Osservazioni

Un campo in un documento Word è una struttura complessa composta da più nodi che includono l'inizio del campo, il codice di campo, il separatore di campo, il risultato e la fine del campo. I campi possono essere annidati, contenere contenuti avanzati e occupare più paragrafi o sezioni di un documento.`Field` La classe è un oggetto "facciata" che fornisce proprietà e metodi che consentono di lavorare con un campo come un singolo oggetto.

IL[`Start`](./start/) ,[`Separator`](./separator/) E[`End`](./end/) le proprietà puntano rispettivamente ai nodi di inizio, separatore e fine del campo .

Il contenuto tra l'inizio e il separatore del campo è il codice di campo. Il contenuto tra il separatore di campo e la fine del campo è il risultato del campo. Il codice di campo è in genere costituito da uno o più [`Run`](../../aspose.words/run/) Oggetti che specificano istruzioni. L'applicazione di elaborazione deve eseguire il codice di campo x000d per calcolare il risultato del campo.

Il processo di calcolo dei risultati dei campi è chiamato aggiornamento di campo. Aspose.Words può aggiornare i risultati field della maggior parte dei tipi di campo esattamente nello stesso modo di Microsoft Word. In particolare, Aspose.Words può calcolare i risultati anche dei campi formula più complessi. Per calcolare il risultato field di un singolo campo, utilizzare[`Update`](./update/) metodo. Per aggiornare i campi nell'intero documento utilizzare[`UpdateFields`](../../aspose.words/document/updatefields/).

È possibile ottenere la versione in testo normale del codice di campo utilizzando[`GetFieldCode`](./getfieldcode/)metodo. È possibile ottenere e impostare la versione in testo normale del risultato del campo utilizzando[`Result`](./result/) property. Sia il codice di campo che il risultato del campo possono contenere contenuti complessi, come campi annidati, paragrafi, forme, tabelle e in questo caso potresti voler lavorare direttamente con i nodi del campo se hai bisogno di un maggiore controllo.

Non si creano istanze di`Field` classe direttamente. Per creare un nuovo campo utilizzare[`InsertField`](../../aspose.words/documentbuilder/insertfield/) metodo.

## Esempi

Mostra come inserire un campo in un documento utilizzando un codice di campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Questo sovraccarico del metodo InsertField aggiorna automaticamente i campi inseriti.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
