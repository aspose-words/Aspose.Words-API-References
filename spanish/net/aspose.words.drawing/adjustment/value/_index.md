---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words para .NET
description: Descubra la propiedad Valor de ajuste, obtenga o configure fácilmente valores de ajuste sin procesar para mejorar la gestión de sus datos y agilizar sus procesos.
type: docs
weight: 20
url: /es/net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

Obtiene o establece el valor bruto del ajuste.

```csharp
public int Value { get; set; }
```

## Observaciones

Un valor de ajuste es simplemente una guía que tiene una fórmula basada en valores especificados. Es decir, no se realiza ningún cálculo para una guía de valor de ajuste. En cambio, esta guía especifica un valor de parámetro que se utiliza para los cálculos dentro de las guías de forma.

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
