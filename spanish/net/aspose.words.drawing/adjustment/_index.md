---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Adjustment, diseñada para mejorar sus formas con valores de ajuste precisos para un formato de documento superior.
type: docs
weight: 700
url: /es/net/aspose.words.drawing/adjustment/
---
## Adjustment class

Representa los valores de ajuste que se aplican a la forma especificada.

```csharp
public class Adjustment
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | Obtiene el nombre del ajuste. |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | Obtiene o establece el valor bruto del ajuste. |

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
