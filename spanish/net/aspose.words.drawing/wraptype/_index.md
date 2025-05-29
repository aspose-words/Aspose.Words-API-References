---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words para .NET
description: Descubra cómo la enumeración Aspose.Words.Drawing.WrapType mejora el ajuste de texto alrededor de formas e imágenes para lograr un formato de documento profesional.
type: docs
weight: 1810
url: /es/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Especifica cómo se ajusta el texto alrededor de una forma o imagen.

```csharp
public enum WrapType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `3` | No se ajusta el texto alrededor de la forma. La forma se coloca detrás o delante del texto. |
| Inline | `0` | La forma permanece en la misma capa que el texto y se trata como un carácter. |
| TopBottom | `1` | El texto se detiene en la parte superior de la forma y reinicia en la línea debajo de la forma. |
| Square | `2` | Envuelve el texto alrededor de todos los lados del cuadro delimitador cuadrado de la forma. |
| Tight | `4` | Se ajusta firmemente alrededor de los bordes de la forma, en lugar de ajustarse alrededor del cuadro delimitador. |
| Through | `5` | Igual que Tight, pero se envuelve dentro de cualquier parte de la forma que esté abierta. |

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

Muestra cómo insertar una imagen y usarla como marca de agua.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta la imagen en el encabezado para que sea visible en todas las páginas.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

//Coloca la imagen en el centro de la página.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Ver también

* property [WrapType](../shapebase/wraptype/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
