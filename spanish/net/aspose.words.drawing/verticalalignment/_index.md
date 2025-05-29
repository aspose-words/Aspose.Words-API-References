---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.VerticalAlignment para una alineación vertical precisa de marcos de texto y tablas en sus documentos. ¡Mejore el control del diseño!
type: docs
weight: 1790
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
| None | `0` | El objeto se posiciona explícitamente, generalmente utilizando su**Arriba** propiedad. |
| Top | `1` | Especifica que el objeto debe estar en la parte superior de la base de alineación vertical. |
| Center | `2` | Especifica que el objeto debe estar centrado con respecto a la base de alineación vertical. |
| Bottom | `3` | Especifica que el objeto debe estar en la parte inferior de la base de alineación vertical. |
| Inside | `4` | Especifica que el objeto debe estar dentro de la base de alineación horizontal. |
| Outside | `5` | Especifica que el objeto debe estar fuera de la base de alineación vertical. |
| Inline | `-1` | No documentado. Parece ser un valor posible para párrafos y tablas flotantes. |
| Default | `0` | Lo mismo queNone . |

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

* property [VerticalAlignment](../shapebase/verticalalignment/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
