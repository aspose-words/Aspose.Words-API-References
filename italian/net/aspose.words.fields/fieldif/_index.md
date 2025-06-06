---
title: FieldIf Class
linktitle: FieldIf
articleTitle: FieldIf
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldIf implementa in modo efficiente i campi IF per migliorare l'automazione dei documenti e semplificare il flusso di lavoro.
type: docs
weight: 2410
url: /it/net/aspose.words.fields/fieldif/
---
## FieldIf class

Implementa il campo IF.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldIf : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldIf](fieldif/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldif/comparisonoperator/) { get; set; } | Ottiene o imposta l'operatore di confronto. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [FalseText](../../aspose.words.fields/fieldif/falsetext/) { get; set; } | Ottiene o imposta il testo visualizzato se l'espressione di confronto è`falso` . |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LeftExpression](../../aspose.words.fields/fieldif/leftexpression/) { get; set; } | Ottiene o imposta la parte sinistra dell'espressione di confronto. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [RightExpression](../../aspose.words.fields/fieldif/rightexpression/) { get; set; } | Ottiene o imposta la parte corretta dell'espressione di confronto. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [TrueText](../../aspose.words.fields/fieldif/truetext/) { get; set; } | Ottiene o imposta il testo visualizzato se l'espressione di confronto è vera. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [EvaluateCondition](../../aspose.words.fields/fieldif/evaluatecondition/)() | Valuta la condizione. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo nodo figlio del suo nodo padre, restituisce il paragrafo padre. Se il campo è già stato rimosso, restituisce`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Esegue un aggiornamento di campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |

## Osservazioni

Confronta i valori designati dalle espressioni[`LeftExpression`](./leftexpression/) E[`RightExpression`](./rightexpression/) in confronto utilizzando l'operatore designato da[`ComparisonOperator`](./comparisonoperator/).

Un campo nel seguente formato verrà utilizzato come origine della stampa unione: { SE 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

## Esempi

Mostra come inserire un campo SE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// Il campo IF visualizzerà una stringa dalla sua proprietà "TrueText",
// o la sua proprietà "FalseText", a seconda della veridicità dell'affermazione che abbiamo costruito.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// In questo caso, "0 = 1" non è corretto, quindi il risultato visualizzato sarà "Falso".
Assert.AreEqual(" IF  0 = 1 True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.False, field.EvaluateCondition());
Assert.AreEqual("False", field.Result);

builder.Write("\nStatement 2: ");
field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// Questa volta l'affermazione è corretta, quindi il risultato visualizzato sarà "True".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
