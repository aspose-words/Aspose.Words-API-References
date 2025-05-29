---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words para .NET
description: Descubra la propiedad Nombre de ajuste para acceder y administrar fácilmente sus ajustes para mejorar la eficiencia y optimizar los flujos de trabajo.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/adjustment/name/
---
## Adjustment.Name property

Obtiene el nombre del ajuste.

```csharp
public string Name { get; }
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

* class [Adjustment](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
