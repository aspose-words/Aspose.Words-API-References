---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words per .NET
description: Aspose.Words.Fields.Field classe. Rappresenta un campo documento di Microsoft Word in C#.
type: docs
weight: 1510
url: /it/net/aspose.words.fields/field/
---
## Field class

Rappresenta un campo documento di Microsoft Word.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class Field
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Restituisce il testo compreso tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi secondari. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce`nullo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/#update)() | Esegue l'aggiornamento del campo. Genera un risultato se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Esegue un aggiornamento del campo. Genera un risultato se il campo è già in fase di aggiornamento. |

## Osservazioni

Un campo in un documento di Word è una struttura complessa composta da più nodi che includono inizio campo, codice campo , separatore campo, risultato campo e fine campo. I campi possono essere nidificati, contenere contenuti avanzati e estendersi su più paragrafi o sezioni in un documento. IL`Field` class è un oggetto "facciata" che fornisce proprietà e metodi che consentono di lavorare con un campo come un singolo oggetto.

IL[`Start`](./start/) ,[`Separator`](./separator/) E[`End`](./end/) le proprietà puntano rispettivamente ai nodi iniziale, separatore e finale del campo .

Il contenuto tra l'inizio del campo e il separatore è il codice di campo. Il contenuto tra il separatore di campo e la fine del campo è il risultato del campo. Il codice di campo in genere è costituito da uno o più [`Run`](../../aspose.words/run/) oggetti che specificano istruzioni. Si prevede che l'applicazione di elaborazione esegua il codice di campo per calcolare il risultato del campo.

Il processo di calcolo dei risultati del campo è chiamato aggiornamento del campo. Aspose.Words può aggiornare i risultati field della maggior parte dei tipi di campo esattamente nello stesso modo in cui lo fa Microsoft Word. In particolare, Aspose.Words può calcolare i risultati anche dei campi formula più complessi. Per calcolare il risultato field di un singolo campo utilizzare il file[`Update`](./update/) metodo. Per aggiornare i campi nell'intero documento utilizzare[`UpdateFields`](../../aspose.words/document/updatefields/).

È possibile ottenere la versione in testo semplice del codice di campo utilizzando il file[`GetFieldCode`](./getfieldcode/) metodo. È possibile ottenere e impostare la versione in testo semplice del risultato del campo utilizzando il metodo[`Result`](./result/) property. Sia il codice del campo che il risultato del campo possono contenere contenuti complessi, come campi nidificati, paragrafi, forme, tabelle e in questo caso potresti voler lavorare direttamente con i nodi del campo se hai bisogno di maggiore controllo.

Non crei istanze di`Field` class direttamente. Per creare un nuovo campo utilizzare il file[`InsertField`](../../aspose.words/documentbuilder/insertfield/) metodo.

## Esempi

Mostra come inserire un campo in un documento utilizzando un codice di campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Questo sovraccarico del metodo InsertField aggiorna automaticamente i campi inseriti.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
