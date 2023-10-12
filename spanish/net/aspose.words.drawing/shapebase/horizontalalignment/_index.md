---
title: ShapeBase.HorizontalAlignment
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Especifica cómo se coloca la forma horizontalmente.
type: docs
weight: 220
url: /es/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Especifica cómo se coloca la forma horizontalmente.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

### Observaciones

El valor predeterminado esNone.

Tiene efecto sólo para formas flotantes de nivel superior.

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

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


