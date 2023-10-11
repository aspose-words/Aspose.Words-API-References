---
title: FieldShape.Text
second_title: Aspose.Words per .NET API Reference
description: FieldShape proprietà. Ottiene o imposta il testo da recuperare.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

Ottiene o imposta il testo da recuperare.

```csharp
public string Text { get; set; }
```

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

// Se abilitiamo una lingua di modifica da destra a sinistra in Microsoft Word, i nostri campi visualizzeranno numeri.
// Altrimenti, verrà visualizzato "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Mostra come vengono gestiti alcuni campi di Microsoft Word meno recenti come SHAPE e EMBED durante il caricamento.

```csharp
// Apre un documento creato in Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Se apriamo il documento Word e premiamo Alt+F9, vedremo un campo SHAPE e un campo EMBED.
// Un campo SHAPE è l'ancora/tela per un oggetto AutoShape con lo stile di disposizione "In linea con il testo" abilitato.
// Un campo EMBED ha la stessa funzione, ma per un oggetto incorporato,
// come un foglio di calcolo da un documento Excel esterno.
// Tuttavia, questi campi non verranno visualizzati nella raccolta Fields del documento.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Questi campi sono supportati solo dalle versioni precedenti di Microsoft Word.
// Il processo di caricamento del documento convertirà questi campi in oggetti Shape,
// a cui possiamo accedere nella raccolta dei nodi del documento.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Il primo nodo Shape corrisponde al campo SHAPE nel documento di input,
// che è l'area di disegno incorporata per AutoShape.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Il secondo nodo Forma è la forma stessa.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// La terza forma è il campo EMBED che conteneva il foglio di calcolo esterno.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Guarda anche

* class [FieldShape](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldshape/)
* assemblea [Aspose.Words](../../../)


