---
title: ShapeBase.RelativeVerticalPosition
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Especifica en relación a qué forma se coloca verticalmente.
type: docs
weight: 410
url: /es/net/aspose.words.drawing/shapebase/relativeverticalposition/
---
## ShapeBase.RelativeVerticalPosition property

Especifica en relación a qué forma se coloca verticalmente.

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; set; }
```

### Observaciones

El valor predeterminado esParagraph.

Solo tiene efecto para las formas flotantes de nivel superior.

### Ejemplos

Muestra cómo insertar una imagen flotante en el centro de una página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una imagen flotante que aparecerá detrás del texto superpuesto y alinéala con el centro de la página.
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

* enum [RelativeVerticalPosition](../../relativeverticalposition/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


