---
title: HorizontalRuleFormat.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words para .NET
description: Descubra la propiedad Alineación HorizontalRuleFormat para personalizar fácilmente la alineación de las reglas horizontales para una mayor flexibilidad de diseño.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

Obtiene o establece la alineación de la regla horizontal.

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

## Observaciones

El valor predeterminado esLeft.

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
