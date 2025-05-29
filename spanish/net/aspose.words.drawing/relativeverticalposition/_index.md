---
title: RelativeVerticalPosition Enum
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.RelativeVerticalPosition para definir el posicionamiento vertical de formas y marcos de texto de manera efectiva y mejorar los diseños de documentos.
type: docs
weight: 1600
url: /es/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

Especifica con respecto a qué es relativa la posición vertical de una forma o marco de texto.

```csharp
public enum RelativeVerticalPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Margin | `0` | Especifica que el posicionamiento vertical será relativo a los márgenes de la página. |
| Page | `1` | El objeto está posicionado en relación con el borde superior de la página. |
| Paragraph | `2` | El objeto se posiciona en relación con la parte superior del párrafo que contiene el ancla. |
| Line | `3` | Sin documentar. |
| TopMargin | `4` | Especifica que el posicionamiento vertical será relativo al margen superior de la página actual. |
| BottomMargin | `5` | Especifica que el posicionamiento vertical será relativo al margen inferior de la página actual. |
| InsideMargin | `6` | Especifica que el posicionamiento vertical será relativo al margen interior de la página actual. |
| OutsideMargin | `7` | Especifica que el posicionamiento vertical será relativo al margen exterior de la página actual. |
| TableDefault | `0` | El valor predeterminado esMargin. |
| TextFrameDefault | `2` | El valor predeterminado esParagraph. |

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

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
