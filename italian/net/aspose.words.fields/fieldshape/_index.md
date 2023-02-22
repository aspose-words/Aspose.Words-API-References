---
title: Class FieldShape
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.FieldShape classe. Implementa il campo SHAPE.
type: docs
weight: 2260
url: /it/net/aspose.words.fields/fieldshape/
---
## FieldShape class

Implementa il campo SHAPE.

```csharp
public class FieldShape : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldShape](fieldshape/)() | Default_Costruttore |

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
| [Text](../../aspose.words.fields/fieldshape/text/) { get; set; } | Ottiene o imposta il testo da recuperare. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Recupera il testo specificato.

### Esempi

Mostra come creare elenchi compatibili con la lingua da destra a sinistra con i campi BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il campo BIDIOUTLINE numera i paragrafi come i campi AUTONUM/LISTNUM,
// ma è visibile solo quando è abilitata una lingua di modifica da destra a sinistra, come l'ebraico o l'arabo.
// Il campo seguente visualizzerà ".1", l'equivalente RTL del numero di elenco "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Aggiungi altri due campi BIDIOUTLINE, che visualizzeranno ".2" e ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Imposta l'allineamento orizzontale del testo per ogni paragrafo del documento su RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Se abilitiamo una lingua di modifica da destra a sinistra in Microsoft Word, i nostri campi visualizzeranno dei numeri.
// Altrimenti visualizzeranno "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Mostra come vengono gestiti alcuni vecchi campi di Microsoft Word come SHAPE ed EMBED durante il caricamento.

```csharp
// Apre un documento creato in Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Se apriamo il documento di Word e premiamo Alt+F9, vedremo un campo SHAPE e un campo EMBED.
// Un campo SHAPE è l'ancora/canvas per un oggetto AutoShape con lo stile di wrapping "In linea con il testo" abilitato.
// Un campo EMBED ha la stessa funzione, ma per un oggetto incorporato,
// come un foglio di calcolo da un documento Excel esterno.
// Tuttavia, questi campi non verranno visualizzati nella raccolta Campi del documento.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Questi campi sono supportati solo dalle vecchie versioni di Microsoft Word.
// Il processo di caricamento del documento convertirà questi campi in oggetti Shape,
// a cui possiamo accedere nella raccolta di nodi del documento.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Il primo nodo Shape corrisponde al campo SHAPE nel documento di input,
// che è la tela inline per la forma.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Il secondo nodo Shape è la forma stessa.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// La terza forma è il campo EMBED che conteneva il foglio di calcolo esterno.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


