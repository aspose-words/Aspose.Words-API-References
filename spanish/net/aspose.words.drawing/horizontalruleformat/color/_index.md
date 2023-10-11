---
title: HorizontalRuleFormat.Color
second_title: Referencia de API de Aspose.Words para .NET
description: HorizontalRuleFormat propiedad. Obtiene o establece el color del pincel que llena la regla horizontal.
type: docs
weight: 20
url: /es/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Obtiene o establece el color del pincel que llena la regla horizontal.

```csharp
public Color Color { get; set; }
```

### Observaciones

Este es un atajo hacia el[`Color`](../../fill/color/) propiedad.

El valor predeterminado es Gray.

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


