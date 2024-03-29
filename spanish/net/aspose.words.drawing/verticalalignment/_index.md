---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.VerticalAlignment enumeración. Especifica la alineación vertical de una forma flotante un marco de texto o una tabla flotante en C#.
type: docs
weight: 1380
url: /es/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Especifica la alineación vertical de una forma flotante, un marco de texto o una tabla flotante.

```csharp
public enum VerticalAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El objeto se posiciona explícitamente, generalmente usando su**Arriba** propiedad. |
| Top | `1` | Especifica que el objeto estará en la parte superior de la base de alineación vertical. |
| Center | `2` | Especifica que el objeto estará centrado con respecto a la base de alineación vertical. |
| Bottom | `3` | Especifica que el objeto estará en la parte inferior de la base de alineación vertical. |
| Inside | `4` | Especifica que el objeto estará dentro de la base de alineación horizontal. |
| Outside | `5` | Especifica que el objeto estará fuera de la base de alineación vertical. |
| Inline | `-1` | No documentado. Parece ser un valor posible para tablas y párrafos flotantes. |
| Default | `0` | Igual queNone . |

## Ejemplos

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

* property [VerticalAlignment](../shapebase/verticalalignment/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
