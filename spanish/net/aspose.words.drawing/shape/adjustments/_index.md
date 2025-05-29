---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: Aspose.Words para .NET
description: Descubra los ajustes de forma. Acceda a valores sin procesar para realizar modificaciones de forma precisas. Mejore fácilmente sus diseños con ajustes personalizados para obtener resultados óptimos.
type: docs
weight: 20
url: /es/net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

Proporciona acceso a los valores brutos de ajuste de una forma. Para una forma que no contiene ningún valor bruto de ajuste, devuelve una colección vacía.

```csharp
public AdjustmentCollection Adjustments { get; }
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

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
