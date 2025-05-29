---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.RelativeHorizontalPosition para definir el posicionamiento horizontal preciso de formas y marcos de texto en sus documentos.
type: docs
weight: 1580
url: /es/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Especifica con respecto a qué es relativa la posición horizontal de una forma o marco de texto.

```csharp
public enum RelativeHorizontalPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Margin | `0` | Especifica que el posicionamiento horizontal debe ser relativo a los márgenes de la página. |
| Page | `1` | El objeto está posicionado con relación al borde izquierdo de la página. |
| Column | `2` | El objeto se posiciona con respecto al lado izquierdo de la columna. |
| Character | `3` | El objeto se posiciona con respecto al lado izquierdo del párrafo. |
| LeftMargin | `4` | Especifica que el posicionamiento horizontal debe ser relativo al margen izquierdo de la página. |
| RightMargin | `5` | Especifica que el posicionamiento horizontal debe ser relativo al margen derecho de la página. |
| InsideMargin | `6` | Especifica que el posicionamiento horizontal debe ser relativo al margen interior de la página actual (el margen izquierdo en las páginas impares, el derecho en las páginas pares). |
| OutsideMargin | `7` | Especifica que el posicionamiento horizontal debe ser relativo al margen exterior de la página actual (el margen derecho en las páginas impares, el izquierdo en las páginas pares). |
| Default | `2` | El valor predeterminado esColumn . |

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

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
