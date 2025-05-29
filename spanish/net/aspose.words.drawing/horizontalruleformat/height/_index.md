---
title: HorizontalRuleFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words para .NET
description: Ajusta la altura de tu regla horizontal fácilmente. Explora la propiedad Altura para personalizar el diseño de tus proyectos web. ¡Mejora tu diseño hoy mismo!
type: docs
weight: 30
url: /es/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

Obtiene o establece la altura de la regla horizontal.

```csharp
public double Height { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza cuando el argumento está fuera del rango de valores válidos. |

## Observaciones

Este es un acceso directo a la[`Height`](../../shapebase/height/) propiedad.

Los valores válidos oscilan entre 0 y 1584 inclusive.

El valor predeterminado es 1,5.

## Ejemplos

Muestra cómo insertar una regla horizontal y personalizar su formato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertHorizontalRule();

HorizontalRuleFormat horizontalRuleFormat = shape.HorizontalRuleFormat;
horizontalRuleFormat.Alignment = HorizontalRuleAlignment.Center;
horizontalRuleFormat.WidthPercent = 70;
horizontalRuleFormat.Height = 3;
horizontalRuleFormat.Color = Color.Blue;
horizontalRuleFormat.NoShade = true;

Assert.True(shape.IsHorizontalRule);
Assert.True(shape.HorizontalRuleFormat.NoShade);
```

### Ver también

* class [HorizontalRuleFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
