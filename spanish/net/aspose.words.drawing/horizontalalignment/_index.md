---
title: Enum HorizontalAlignment
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.HorizontalAlignment enumeración. Especifica la alineación horizontal de una forma flotante marco de texto o tabla flotante.
type: docs
weight: 900
url: /es/net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

Especifica la alineación horizontal de una forma flotante, marco de texto o tabla flotante.

```csharp
public enum HorizontalAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El objeto se posiciona explícitamente, generalmente usando su **Izquierda** propiedad. |
| Default | `0` | Igual queNone . |
| Left | `1` | Especifica que el objeto se alineará a la izquierda con respecto a la base de alineación horizontal. |
| Center | `2` | Especifica que el objeto debe estar centrado con respecto a la base de alineación horizontal. |
| Right | `3` | Especifica que el objeto se alineará a la derecha con respecto a la base de alineación horizontal. |
| Inside | `4` | Especifica que el objeto estará dentro de la base de alineación horizontal. |
| Outside | `5` | Especifica que el objeto estará fuera de la base de alineación horizontal. |

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

* property [HorizontalAlignment](../shapebase/horizontalalignment/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)


