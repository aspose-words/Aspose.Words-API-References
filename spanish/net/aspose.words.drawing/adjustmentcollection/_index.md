---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.AdjustmentCollection su solución para administrar valores de ajuste de solo lectura para formas. ¡Mejore el diseño de sus documentos sin esfuerzo!
type: docs
weight: 710
url: /es/net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

Representa una colección de solo lectura de[`Adjustment`](../adjustment/) Ajusta los valores que se aplican a la forma especificada.

```csharp
public class AdjustmentCollection
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | Obtiene el número de elementos contenidos en la colección. |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | Devuelve un ajuste en el índice especificado. |

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
