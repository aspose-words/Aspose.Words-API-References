---
title: Class Field
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.Field classe. Rappresenta un campo di un documento di Microsoft Word.
type: docs
weight: 1360
url: /it/net/aspose.words.fields/field/
---
## Field class

Rappresenta un campo di un documento di Microsoft Word.

```csharp
public class Field
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/#update)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/#update_1)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Un campo in un documento Word è una struttura complessa costituita da più nodi che includono inizio campo, codice campo , separatore campo, risultato campo e fine campo. I campi possono essere nidificati, contenere contenuti avanzati e includere più paragrafi o sezioni in un documento. Il`Field`class è un oggetto "facciata" che fornisce proprietà e metodi che consentono di lavorare con un campo come un singolo oggetto.

Il[`Start`](./start/) ,[`Separator`](./separator/) e[`End`](./end/) le proprietà puntano rispettivamente ai nodi di inizio, separatore e fine del campo .

Il contenuto tra l'inizio del campo e il separatore è il codice del campo. Il contenuto tra il separatore di campo e la fine del campo è il risultato del campo. Il codice di campo è in genere costituito da uno o più [`Run`](../../aspose.words/run/) oggetti che specificano istruzioni. L'applicazione di elaborazione dovrebbe eseguire il codice del campo per calcolare il risultato del campo.

Il processo di calcolo dei risultati del campo è chiamato aggiornamento del campo. Aspose.Words può aggiornare i risultati field della maggior parte dei tipi di campo esattamente nello stesso modo in cui lo fa Microsoft Word. In particolare, Aspose.Words può calcolare i risultati anche dei campi formula più complessi. Per calcolare il risultato field di un singolo campo utilizzare il[`Update`](./update/) metodo. Per aggiornare i campi nell'intero documento utilizzare[`UpdateFields`](../../aspose.words/document/updatefields/).

È possibile ottenere la versione in testo normale del codice di campo utilizzando il[`GetFieldCode`](./getfieldcode/) method. È possibile ottenere e impostare la versione in testo normale del risultato del campo utilizzando il[`Result`](./result/) property. Sia il codice del campo che il risultato del campo possono contenere contenuto complesso, come campi nidificati, paragrafi, forme, tabelle e in questo caso potresti voler lavorare direttamente con i nodi del campo se hai bisogno di maggiore controllo.

Non crei istanze di`Field` class direttamente. Per creare un nuovo campo utilizzare il[`InsertField`](../../aspose.words/documentbuilder/insertfield/) metodo.

### Esempi

Mostra come inserire un campo in un documento utilizzando un codice campo.

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


