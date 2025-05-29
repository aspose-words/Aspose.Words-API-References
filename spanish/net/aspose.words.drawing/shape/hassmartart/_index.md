---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: Aspose.Words para .NET
description: Descubre si tu forma incluye un objeto SmartArt con la propiedad HasSmartArt. ¡Descubre posibilidades de diseño creativo para tus proyectos!
type: docs
weight: 100
url: /es/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Devuelve`verdadero` Si esto[`Shape`](../) tiene un objeto SmartArt.

```csharp
public bool HasSmartArt { get; }
```

## Ejemplos

Muestra cómo contar la cantidad de formas en un documento con objetos SmartArt.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Ver también

* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
