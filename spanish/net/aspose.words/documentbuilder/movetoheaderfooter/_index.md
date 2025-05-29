---
title: DocumentBuilder.MoveToHeaderFooter
linktitle: MoveToHeaderFooter
articleTitle: MoveToHeaderFooter
second_title: Aspose.Words para .NET
description: Navegue sin esfuerzo a los encabezados y pies de página con el método MoveToHeaderFooter de DocumentBuilder, mejorando la eficiencia de la edición de sus documentos.
type: docs
weight: 580
url: /es/net/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder.MoveToHeaderFooter method

Mueve el cursor al comienzo de un encabezado o pie de página en la sección actual.

```csharp
public void MoveToHeaderFooter(HeaderFooterType headerFooterType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | Especifica el encabezado o pie de página al que moverse. |

## Observaciones

Después de mover el cursor a un encabezado o pie de página, puede usar el resto de[`DocumentBuilder`](../) métodos para modificar el contenido del encabezado o pie de página.

Si desea crear encabezados y pies de página diferentes para la primera página, necesita configurar[`DifferentFirstPageHeaderFooter`](../../pagesetup/differentfirstpageheaderfooter/).

Si desea crear encabezados y pies de página diferentes para páginas pares e impares, necesita configurar[`OddAndEvenPagesHeaderFooter`](../../pagesetup/oddandevenpagesheaderfooter/).

Usar[`MoveToSection`](../movetosection/) para pasar del encabezado al texto principal.

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

Muestra cómo crear encabezados y pies de página en un documento utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especificamos que queremos encabezados y pies de página diferentes para la primera página, páginas pares e impares.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Cree los encabezados y luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Ver también

* enum [HeaderFooterType](../../headerfootertype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
