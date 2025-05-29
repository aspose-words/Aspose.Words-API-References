---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words para .NET
description: Descubre la propiedad Font TintAndShade para ajustar colores fácilmente. Aclara u oscurece tonos para lograr diseños vibrantes. ¡Mejora tus proyectos sin esfuerzo!
type: docs
weight: 530
url: /es/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Obtiene o establece un valor doble que aclara u oscurece un color.

```csharp
public double TintAndShade { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza si se establece esta propiedad en un valor menor que -1 o mayor que 1. |
| InvalidOperationException | Lanza si se establece esta propiedad para[`Font`](../) objeto con colores no temáticos. |

## Observaciones

Los valores permitidos están en el rango de -1 (más oscuro) a 1 (más claro) para esta propiedad.

Cero (0) es neutral.

## Ejemplos

Muestra cómo crear y utilizar estilos temáticos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Crea algo de estilo con las propiedades de fuente del tema.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
