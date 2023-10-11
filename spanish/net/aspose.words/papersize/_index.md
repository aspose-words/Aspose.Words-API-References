---
title: Enum PaperSize
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.PaperSize enumeración. Especifica el tamaño del papel.
type: docs
weight: 4380
url: /es/net/aspose.words/papersize/
---
## PaperSize enumeration

Especifica el tamaño del papel.

```csharp
public enum PaperSize
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| A3 | `0` | 297 x 420 mm. |
| A4 | `1` | 210 x 297 mm. |
| A5 | `2` | 148 x 210 mm. |
| B4 | `3` | 250 x 353 mm. |
| B5 | `4` | 176 x 250 mm. |
| Executive | `5` | 7,25 x 10,5 pulgadas. |
| Folio | `6` | 8,5 x 13 pulgadas. |
| Ledger | `7` | 17 x 11 pulgadas. |
| Legal | `8` | 8,5 x 14 pulgadas. |
| Letter | `9` | 8,5 x 11 pulgadas. |
| EnvelopeDL | `10` | 110 x 220 mm. |
| Quarto | `11` | 8,47 x 10,83 pulgadas. |
| Statement | `12` | 8,5 x 5,5 pulgadas. |
| Tabloid | `13` | 11 x 17 pulgadas. |
| Paper10x14 | `14` | 10 x 14 pulgadas. |
| Paper11x17 | `15` | 11 x 17 pulgadas. |
| Number10Envelope | `16` | 4,125 x 9,5 pulgadas. |
| Custom | `17` | Tamaño de papel personalizado. |

### Ejemplos

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes y otras configuraciones para una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Muestra cómo configurar los tamaños de página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Podemos cambiar el tamaño de la página actual a un tamaño predefinido
// utilizando la propiedad "PaperSize" del objeto PageSetup de esta sección.
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// Cada sección tiene su propio objeto PageSetup. Cuando utilizamos un generador de documentos para crear una nueva sección,
// el objeto PageSetup de esa sección hereda todos los valores del objeto PageSetup de la sección anterior.
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// Establece un tamaño personalizado para las páginas de esta sección.
builder.PageSetup.PageWidth = 620;
builder.PageSetup.PageHeight = 480;

Assert.AreEqual(PaperSize.Custom, builder.PageSetup.PaperSize);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

doc.Save(ArtifactsDir + "PageSetup.PaperSizes.docx");
```

Muestra cómo construir un documento Aspose.Words a mano.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llama al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

// Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, crea una nueva sección y luego agrégala como secundaria al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Establece algunas propiedades de configuración de página para la sección.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un párrafo, establece algunas propiedades de formato y luego añádelo como elemento secundario al cuerpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finalmente, agrega algo de contenido para hacer el documento. Crea una carrera,
// establece su apariencia y contenido, y luego lo agrega como elemento secundario al párrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


