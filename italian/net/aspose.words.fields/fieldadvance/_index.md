---
title: FieldAdvance
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo ADVANCE.
type: docs
weight: 1390
url: /it/net/aspose.words.fields/fieldadvance/
---
## FieldAdvance class

Implementa il campo ADVANCE.

```csharp
public class FieldAdvance : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldAdvance](fieldadvance)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [DownOffset](../../aspose.words.fields/fieldadvance/downoffset) { get; set; } | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato verso il basso. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [HorizontalPosition](../../aspose.words.fields/fieldadvance/horizontalposition) { get; set; } | Ottiene o imposta il numero di punti in base ai quali il testo che segue il campo deve essere spostato orizzontalmente dal bordo sinistro della colonna, cornice o casella di testo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LeftOffset](../../aspose.words.fields/fieldadvance/leftoffset) { get; set; } | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato a sinistra. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [RightOffset](../../aspose.words.fields/fieldadvance/rightoffset) { get; set; } | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato a destra. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ottiene il tipo di campo di Microsoft Word. |
| [UpOffset](../../aspose.words.fields/fieldadvance/upoffset) { get; set; } | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato verso l'alto. |
| [VerticalPosition](../../aspose.words.fields/fieldadvance/verticalposition) { get; set; } | Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato verticalmente dal bordo superiore della pagina. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Sposta il punto iniziale in cui il testo che segue lessicalmente il campo viene visualizzato a destra oa sinistra, in alto o in basso, o in una specifica posizione orizzontale o verticale.

### Esempi

Mostra come inserire un campo ADVANCE e modificarne le proprietà.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Di seguito sono riportati due modi per utilizzare il campo AVANZAMENTO per regolare la posizione del testo che lo segue.
// Gli effetti di un campo ADVANCE continuano ad essere applicati fino alla fine del paragrafo,
// o un altro campo ADVANCE aggiorna i valori di offset/coordinate.
// 1 - Specificare un offset direzionale:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Sposta il testo in una posizione specificata dalle coordinate:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
