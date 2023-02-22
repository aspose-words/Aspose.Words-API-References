---
title: ShapeBase.IsInline
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Un modo rapido per determinare se questa forma è posizionata in linea con il testo.
type: docs
weight: 280
url: /it/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Un modo rapido per determinare se questa forma è posizionata in linea con il testo.

```csharp
public bool IsInline { get; }
```

### Osservazioni

Ha effetto solo per le forme di livello superiore.

### Esempi

Mostra come determinare se una forma è in linea o mobile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due tipi di avvolgimento che possono avere le forme.
// 1 - In linea:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Una forma in linea si trova all'interno di un paragrafo tra altri elementi di paragrafo, come sequenze di testo.
// In Microsoft Word, possiamo fare clic e trascinare la forma su qualsiasi paragrafo come se fosse un carattere.
// Se la forma è grande, influirà sulla spaziatura verticale del paragrafo.
// Non possiamo spostare questa forma in una posizione senza paragrafo.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Fluttuante:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Una forma mobile appartiene al paragrafo in cui la inseriamo,
// che possiamo determinare da un simbolo di ancoraggio che appare quando facciamo clic sulla forma.
// Se la forma non ha un simbolo di ancoraggio visibile alla sua sinistra,
// dovremo abilitare gli anchor visibili tramite "Opzioni" -> "Visualizza" -> "Ancora oggetto".
// In Microsoft Word, possiamo fare clic con il tasto sinistro e trascinare questa forma liberamente in qualsiasi posizione.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


