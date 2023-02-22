---
title: DocumentBuilder.InsertHorizontalRule
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Inserta una forma de regla horizontal en el documento.
type: docs
weight: 320
url: /es/net/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder.InsertHorizontalRule method

Inserta una forma de regla horizontal en el documento.

```csharp
public Shape InsertHorizontalRule()
```

### Valor_devuelto

La forma que es una regla horizontal.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


