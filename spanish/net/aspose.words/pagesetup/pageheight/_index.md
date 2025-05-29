---
title: PageSetup.PageHeight
linktitle: PageHeight
articleTitle: PageHeight
second_title: Aspose.Words para .NET
description: Descubra la propiedad PageHeight de PageSetup para administrar de manera eficiente la altura de su documento en puntos, mejorando su diseño y presentación.
type: docs
weight: 310
url: /es/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Devuelve o establece la altura de la página en puntos.

```csharp
public double PageHeight { get; set; }
```

## Ejemplos

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

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
