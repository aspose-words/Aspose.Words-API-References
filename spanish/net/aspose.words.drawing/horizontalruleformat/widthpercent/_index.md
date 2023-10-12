---
title: HorizontalRuleFormat.WidthPercent
second_title: Referencia de API de Aspose.Words para .NET
description: HorizontalRuleFormat propiedad. Obtiene o establece la longitud de la regla horizontal especificada expresada como porcentaje del ancho de la ventana.
type: docs
weight: 50
url: /es/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Obtiene o establece la longitud de la regla horizontal especificada expresada como porcentaje del ancho de la ventana.

```csharp
public double WidthPercent { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza cuando el argumento estaba fuera del rango de valores válidos. |

### Observaciones

Los valores válidos oscilan entre 1 y 100 inclusive.

El valor predeterminado es 100.

### Ejemplos

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

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
* espacio de nombres [Aspose.Words.Drawing](../../horizontalruleformat/)
* asamblea [Aspose.Words](../../../)


