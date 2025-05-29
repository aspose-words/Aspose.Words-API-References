---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsInline di ShapeBase per verificare facilmente se la tua forma è allineata con il testo, migliorando il tuo design e l'efficienza del layout.
type: docs
weight: 310
url: /it/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Un modo rapido per determinare se questa forma è posizionata in linea con il testo.

```csharp
public bool IsInline { get; }
```

## Osservazioni

Ha effetto solo sulle forme di livello superiore.

## Esempi

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

// Una forma in linea si trova all'interno di un paragrafo, tra altri elementi del paragrafo, come ad esempio sequenze di testo.
// In Microsoft Word, possiamo fare clic e trascinare la forma su qualsiasi paragrafo come se fosse un carattere.
// Se la forma è grande, influirà sulla spaziatura verticale dei paragrafi.
// Non possiamo spostare questa forma in una posizione senza paragrafo.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Galleggiante:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Una forma fluttuante appartiene al paragrafo in cui la inseriamo,
// che possiamo determinare tramite un simbolo di ancoraggio che appare quando clicchiamo sulla forma.
// Se la forma non ha un simbolo di ancoraggio visibile alla sua sinistra,
// dovremo abilitare le ancore visibili tramite "Opzioni" -> "Visualizzazione" -> "Ancore oggetto".
// In Microsoft Word, possiamo cliccare con il tasto sinistro del mouse e trascinare liberamente questa forma in qualsiasi posizione.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
