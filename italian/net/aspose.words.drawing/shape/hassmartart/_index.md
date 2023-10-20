---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: Aspose.Words per .NET
description: Shape HasSmartArt proprietà. RestituisceVERO se questoShape ha un oggetto SmartArt in C#.
type: docs
weight: 90
url: /it/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Restituisce`VERO` se questo[`Shape`](../) ha un oggetto SmartArt.

```csharp
public bool HasSmartArt { get; }
```

## Esempi

Mostra come contare il numero di forme in un documento con oggetti SmartArt.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Guarda anche

* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
