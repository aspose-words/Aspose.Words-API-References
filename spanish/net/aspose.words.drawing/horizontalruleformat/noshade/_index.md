---
title: HorizontalRuleFormat.NoShade
second_title: Referencia de API de Aspose.Words para .NET
description: HorizontalRuleFormat propiedad. Indica la presencia de sombreado 3D para la regla horizontal. Si es verdadero entonces la regla horizontal no tiene sombreado 3D y se utiliza un color sólido.
type: docs
weight: 40
url: /es/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Indica la presencia de sombreado 3D para la regla horizontal. Si es verdadero, entonces la regla horizontal no tiene sombreado 3D y se utiliza un color sólido.

```csharp
public bool NoShade { get; set; }
```

### Observaciones

El valor predeterminado es falso.

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


