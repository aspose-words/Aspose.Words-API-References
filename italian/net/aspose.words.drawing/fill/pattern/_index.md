---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: Aspose.Words per .NET
description: Scopri la proprietà Pattern di riempimento per accedere e personalizzare facilmente il PatternType per i tuoi progetti. Arricchisci i tuoi progetti con opzioni di riempimento uniche!
type: docs
weight: 160
url: /it/net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

Ottiene un[`PatternType`](../../patterntype/) per il riempimento.

```csharp
public PatternType Pattern { get; }
```

## Esempi

Mostra come impostare un pattern per una forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Esistono diversi modi per specificare il riempimento di un pattern.
// 1 - Applica il motivo al riempimento della forma:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Applica il motivo con colori di primo piano e di sfondo al riempimento della forma:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Guarda anche

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
