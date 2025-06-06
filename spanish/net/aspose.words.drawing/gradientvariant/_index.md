---
title: GradientVariant Enum
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.GradientVariant para rellenos degradados personalizables y mejorar los diseños de sus documentos con estilos vibrantes.
type: docs
weight: 1340
url: /es/net/aspose.words.drawing/gradientvariant/
---
## GradientVariant enumeration

Especifica la variante para un relleno degradado.

```csharp
public enum GradientVariant
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Variante de degradado 'Ninguno'. |
| Variant1 | `1` | Variante de degradado 1. |
| Variant2 | `2` | Variante de degradado 2. |
| Variant3 | `3` | Variante de degradado 3. |
| Variant4 | `4` | Variante de degradado 4. |

## Observaciones

Corresponde a las cuatro variantes de la pestaña Degradado del cuadro de diálogo Efectos de relleno en Word.

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
