---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words para .NET
description: Descubre la propiedad BackgroundShape de DocumentBase y personaliza fácilmente la forma del fondo de tu documento para un aspecto visual mejorado. ¡Maximiza tu potencial de diseño!
type: docs
weight: 10
url: /es/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Obtiene o establece la forma del fondo del documento. Puede ser`nulo` .

```csharp
public Shape BackgroundShape { get; set; }
```

## Observaciones

Microsoft Word solo permite una forma que tenga su[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) propiedad igual aRectangle para usarse como forma de fondo para un documento.

Microsoft Word solo admite las propiedades de relleno de una forma de fondo. Se ignoran todas las demás propiedades .

Si se establece esta propiedad en un valor distinto de nulo, también se establecerá la[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) a`verdadero`.

## Ejemplos

Muestra cómo establecer una forma de fondo para cada página de un documento.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

//El único tipo de forma que podemos usar como fondo es un rectángulo.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// Hay dos formas de utilizar esta forma como fondo de página.
// 1 - Un color plano:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - Una imagen:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

//Ajusta la apariencia de la imagen para que sea más adecuada como marca de agua.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word no admite formas con imágenes como fondos,
// pero aún podemos ver estos fondos en otros formatos de guardado como .pdf.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
