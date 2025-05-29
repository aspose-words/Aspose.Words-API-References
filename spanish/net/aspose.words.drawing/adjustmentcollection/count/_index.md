---
title: AdjustmentCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad AdjustmentCollection Count para recuperar fácilmente el número total de elementos y mejorar la eficiencia de la gestión de datos.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/adjustmentcollection/count/
---
## AdjustmentCollection.Count property

Obtiene el número de elementos contenidos en la colección.

```csharp
public int Count { get; }
```

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

* class [AdjustmentCollection](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
