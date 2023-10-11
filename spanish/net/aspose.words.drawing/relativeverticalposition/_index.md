---
title: Enum RelativeVerticalPosition
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.RelativeVerticalPosition enumeración. Especifica con qué es relativa la posición vertical de una forma o marco de texto.
type: docs
weight: 1210
url: /es/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

Especifica con qué es relativa la posición vertical de una forma o marco de texto.

```csharp
public enum RelativeVerticalPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Margin | `0` | Especifica que la posición vertical será relativa a los márgenes de la página. |
| Page | `1` | El objeto está colocado en relación con el borde superior de la página. |
| Paragraph | `2` | El objeto está ubicado en relación con la parte superior del párrafo que contiene el ancla. |
| Line | `3` | Indocumentado. |
| TopMargin | `4` | Especifica que la posición vertical será relativa al margen superior de la página actual. |
| BottomMargin | `5` | Especifica que la posición vertical será relativa al margen inferior de la página actual. |
| InsideMargin | `6` | Especifica que la posición vertical será relativa al margen interior de la página actual. |
| OutsideMargin | `7` | Especifica que la posición vertical será relativa al margen exterior de la página actual. |
| TableDefault | `0` | El valor predeterminado esMargin . |
| TextFrameDefault | `2` | El valor predeterminado esParagraph . |

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

Muestra cómo insertar una imagen y utilizarla como marca de agua.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta la imagen en el encabezado para que sea visible en todas las páginas.
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Coloca la imagen en el centro de la página.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Muestra cómo insertar una imagen y usarla como marca de agua (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta la imagen en el encabezado para que sea visible en todas las páginas.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // Coloca la imagen en el centro de la página.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### Ver también

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)


