---
title: Fill.GradientVariant
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: Aspose.Words para .NET
description: Fill GradientVariant propiedad. Obtiene la variante de gradienteGradientVariant para el relleno en C#.
type: docs
weight: 120
url: /es/net/aspose.words.drawing/fill/gradientvariant/
---
## Fill.GradientVariant property

Obtiene la variante de gradiente[`GradientVariant`](../../gradientvariant/) para el relleno.

```csharp
public GradientVariant GradientVariant { get; }
```

## Ejemplos

Muestra cómo rellenar una forma con degradados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Aplicar relleno degradado de un color a la forma con ForeColor de relleno degradado.
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
// el relleno degradado no obtiene ningún efecto, funcionará solo para degradado lineal.
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

* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
