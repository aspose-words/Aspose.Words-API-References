---
title: HorizontalRuleFormat.NoShade
linktitle: NoShade
articleTitle: NoShade
second_title: Aspose.Words para .NET
description: Descubra la propiedad HorizontalRuleFormat NoShade, que controla el sombreado 3D de las líneas horizontales. ¡Consiga un diseño elegante y de colores sólidos sin esfuerzo!
type: docs
weight: 40
url: /es/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Indica la presencia de sombreado 3D para la regla horizontal. Si`verdadero` , entonces la regla horizontal no tiene sombreado 3D y se usa un color sólido.

```csharp
public bool NoShade { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO`.

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
