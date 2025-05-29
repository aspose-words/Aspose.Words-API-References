---
title: ShapeBase.HorizontalAlignment
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase HorizontalAlignment para optimizar el posicionamiento horizontal de las formas en su diseño para un mejor control del diseño.
type: docs
weight: 240
url: /es/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Especifica cómo se posiciona la forma horizontalmente.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

## Observaciones

El valor predeterminado esNone.

Tiene efecto sólo para formas flotantes de nivel superior.

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

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
