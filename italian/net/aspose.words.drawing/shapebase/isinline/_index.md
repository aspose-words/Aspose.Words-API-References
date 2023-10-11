---
title: ShapeBase.IsInline
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Un modo rapido per determinare se questa forma è posizionata in linea con il testo.
type: docs
weight: 290
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

// Di seguito sono riportati due tipi di avvolgimento che le forme possono avere.
// 1 - In linea:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Una forma in linea si trova all'interno di un paragrafo tra gli altri elementi del paragrafo, come le sequenze di testo.
// In Microsoft Word, possiamo fare clic e trascinare la forma su qualsiasi paragrafo come se fosse un carattere.
// Se la forma è grande, influenzerà la spaziatura verticale del paragrafo.
// Non possiamo spostare questa forma in un posto senza paragrafo.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Galleggiante:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Una forma fluttuante appartiene al paragrafo in cui la inseriamo,
// che possiamo determinare da un simbolo di ancoraggio che appare quando facciamo clic sulla forma.
// Se la forma non ha un simbolo di ancoraggio visibile alla sua sinistra,
// dovremo abilitare gli ancoraggi visibili tramite "Opzioni" -> "Visualizza" -> "Ancore di oggetti".
// In Microsoft Word, possiamo fare clic con il tasto sinistro e trascinare questa forma liberamente in qualsiasi posizione.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


