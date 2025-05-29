---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase BehindText para controlar las capas de formas en sus diseños, mejorando la visibilidad del texto y la precisión del diseño sin esfuerzo.
type: docs
weight: 50
url: /es/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Especifica si la forma está debajo o encima del texto.

```csharp
public bool BehindText { get; set; }
```

## Observaciones

Tiene efecto sólo para formas de nivel superior.

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo insertar una imagen flotante en el centro de una página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una imagen flotante que aparecerá detrás del texto superpuesto y la alinea con el centro de la página.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
