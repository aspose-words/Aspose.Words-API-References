---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase AnchorLocked per controllare il blocco dell'ancoraggio per le forme, migliorando la stabilità del design e la flessibilità nei tuoi progetti.
type: docs
weight: 30
url: /it/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Specifica se l'ancoraggio della forma è bloccato.

```csharp
public bool AnchorLocked { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`.

Ha effetto solo sulle forme di livello superiore.

Questa proprietà influenza il comportamento dell'ancoraggio della forma in Microsoft Word. Quando l'ancoraggio non è bloccato, spostando la forma in Microsoft Word è possibile spostare anche l'ancoraggio della forma.

## Esempi

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
// si sposti quando si sposta la forma in Microsoft Word.
// Imposta la proprietà "AnchorLocked" su "false" per consentire qualsiasi movimento della forma
// per spostare anche il suo ancoraggio su qualsiasi altro paragrafo vicino al quale la forma finisce.
shape.AnchorLocked = anchorLocked;

// Se la forma non ha un simbolo di ancoraggio visibile alla sua sinistra,
// dovremo abilitare le ancore visibili tramite "Opzioni" -> "Visualizzazione" -> "Ancore oggetto".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
