---
title: GradientStyle Enum
linktitle: GradientStyle
articleTitle: GradientStyle
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.GradientStyle para obtener estilos de relleno degradado personalizables y mejorar los diseños de sus documentos con imágenes vibrantes.
type: docs
weight: 1330
url: /es/net/aspose.words.drawing/gradientstyle/
---
## GradientStyle enumeration

Especifica el estilo de un relleno degradado.

```csharp
public enum GradientStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `-1` | Sin gradiente. |
| Horizontal | `1` | Degradado que se extiende horizontalmente a través de un objeto. |
| Vertical | `2` | Gradiente que corre verticalmente hacia abajo por un objeto. |
| DiagonalUp | `3` | Degradado diagonal que se mueve desde una esquina inferior hasta la esquina opuesta. |
| DiagonalDown | `4` | Degradado diagonal que se mueve desde una esquina superior hacia la esquina opuesta. |
| FromCorner | `5` | Gradiente que va desde una esquina a las otras tres esquinas. |
| FromCenter | `6` | Degradado que va desde el centro hacia las esquinas. |

## Ejemplos

Muestra cómo rellenar una forma con degradados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Aplicar relleno degradado de un color a la forma con ForeColor del relleno degradado.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Aplicar relleno degradado de dos colores a la forma.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Cambia el color de fondo del relleno degradado.
shape.Fill.BackColor = Color.Yellow;
// Tenga en cuenta que cambia "GradientAngle" por "GradientStyle.FromCorner/GradientStyle.FromCenter"
// El relleno de degradado no tiene ningún efecto, solo funcionará con degradado lineal.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Utilice la opción de cumplimiento para definir la forma usando DML si desea obtener "GradientStyle",
// Propiedades "GradientVariant" y "GradientAngle" después de guardar el documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
