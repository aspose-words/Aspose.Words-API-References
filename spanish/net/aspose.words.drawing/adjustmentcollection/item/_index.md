---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Descubra la propiedad Item AdjustmentCollection, recupere fácilmente ajustes por índice para una administración de datos perfecta y un rendimiento mejorado.
type: docs
weight: 20
url: /es/net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

Devuelve un ajuste en el índice especificado.

```csharp
public Adjustment this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Un índice de la colección. |

## Ejemplos

Muestra cómo trabajar con valores brutos de ajuste.

```csharp
Document doc = new Document(MyDir + "Rounded rectangle shape.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

AdjustmentCollection adjustments = shape.Adjustments;
Assert.AreEqual(1, adjustments.Count);

Adjustment adjustment = adjustments[0];
Assert.AreEqual("adj", adjustment.Name);
Assert.AreEqual(16667, adjustment.Value);

adjustment.Value = 30000;

doc.Save(ArtifactsDir + "Shape.Adjustments.docx");
```

### Ver también

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
