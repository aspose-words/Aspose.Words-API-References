---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: Aspose.Words per .NET
description: Scopri se la tua forma include un oggetto SmartArt con la proprietà HasSmartArt. Sblocca nuove possibilità di design creativo per i tuoi progetti!
type: docs
weight: 100
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
