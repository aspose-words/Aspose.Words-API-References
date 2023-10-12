---
title: Shape.HasSmartArt
second_title: Aspose.Words per .NET API Reference
description: Shape proprietà. RestituisceVERO se questoShape ha un oggetto SmartArt.
type: docs
weight: 90
url: /it/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Restituisce`VERO` se questo[`Shape`](../) ha un oggetto SmartArt.

```csharp
public bool HasSmartArt { get; }
```

### Esempi

Mostra come contare il numero di forme in un documento con oggetti SmartArt.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Guarda anche

* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shape/)
* assemblea [Aspose.Words](../../../)


