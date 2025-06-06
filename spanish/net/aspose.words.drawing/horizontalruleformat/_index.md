---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words para .NET
description: Descubre la clase Aspose.Words.Drawing.HorizontalRuleFormat para un formato de línea horizontal avanzado. ¡Mejora el diseño de tus documentos sin esfuerzo!
type: docs
weight: 1380
url: /es/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Representa el formato de regla horizontal.

Para obtener más información, visite el[Trabajando con formas](https://docs.aspose.com/words/net/working-with-shapes/) Artículo de documentación.

```csharp
public class HorizontalRuleFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Obtiene o establece la alineación de la regla horizontal. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Obtiene o establece el color del pincel que rellena la regla horizontal. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Obtiene o establece la altura de la regla horizontal. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Indica la presencia de sombreado 3D para la regla horizontal. Si`verdadero` , entonces la regla horizontal no tiene sombreado 3D y se usa un color sólido. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Obtiene o establece la longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana. |

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
