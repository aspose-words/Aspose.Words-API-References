---
title: ShapeBase.AnchorLocked
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Specifica se lancoraggio della forma è bloccato.
type: docs
weight: 30
url: /it/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Specifica se l'ancoraggio della forma è bloccato.

```csharp
public bool AnchorLocked { get; set; }
```

### Osservazioni

Il valore predefinito è`falso`.

Ha effetto solo per le forme di livello superiore.

Questa proprietà influisce sul comportamento dell'ancora della forma in Microsoft Word. Quando l'ancora non è bloccata, lo spostamento della forma in Microsoft Word può spostare anche l'ancora della forma.

### Esempi

Mostra come bloccare o sbloccare l'ancoraggio del paragrafo di una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Imposta la proprietà "AnchorLocked" su "true" per impedire l'ancoraggio della forma
// dallo spostamento quando si sposta la forma in Microsoft Word.
// Imposta la proprietà "AnchorLocked" su "false" per consentire qualsiasi movimento della forma
// per spostare l'ancoraggio anche su qualsiasi altro paragrafo a cui la forma finisce vicino.
shape.AnchorLocked = anchorLocked;

// Se la forma non ha un simbolo di ancoraggio visibile alla sua sinistra,
// dovremo abilitare gli ancoraggi visibili tramite "Opzioni" -> "Visualizza" -> "Ancore di oggetti".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


