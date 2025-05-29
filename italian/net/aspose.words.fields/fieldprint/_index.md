---
title: FieldPrint Class
linktitle: FieldPrint
articleTitle: FieldPrint
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldPrint per un'implementazione fluida dei campi PRINT. Migliora l'elaborazione dei tuoi documenti con potenti funzionalità oggi stesso!
type: docs
weight: 2690
url: /it/net/aspose.words.fields/fieldprint/
---
## FieldPrint class

Implementa il campo PRINT.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldPrint : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldPrint](fieldprint/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [PostScriptGroup](../../aspose.words.fields/fieldprint/postscriptgroup/) { get; set; } | Ottiene o imposta il rettangolo di disegno su cui operano le istruzioni PostScript. |
| [PrinterInstructions](../../aspose.words.fields/fieldprint/printerinstructions/) { get; set; } | Ottiene o imposta i caratteri del codice di controllo specifici della stampante o le istruzioni PostScript. |
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

Istruzione per inviare i caratteri del codice di controllo specifici della stampante alla stampante selezionata quando il documento viene stampato.

## Esempi

Mostra come inserire un campo STAMPA.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Il campo PRINT può inviare istruzioni alla stampante.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Imposta l'area su cui la stampante dovrà eseguire le istruzioni.
// In questo caso, sarà il paragrafo a contenere il nostro campo PRINT.
field.PostScriptGroup = "para";

// Quando utilizziamo una stampante che supporta PostScript per stampare il nostro documento,
// questo comando renderà bianca l'intera area specificata in "field.PostScriptGroup".
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
