---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words para .NET
description: PdfSaveOptions PageMode propiedad. Especifica cómo se debe mostrar el documento PDF cuando se abre en el lector de PDF en C#.
type: docs
weight: 250
url: /es/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Especifica cómo se debe mostrar el documento PDF cuando se abre en el lector de PDF.

```csharp
public PdfPageMode PageMode { get; set; }
```

## Observaciones

El valor predeterminado esUseOutlines .

## Ejemplos

Muestra cómo configurar instrucciones que algunos lectores de PDF deben seguir al abrir un documento de salida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "PageMode" en "PdfPageMode.FullScreen" para que el lector de PDF abra el archivo guardado
// documento en modo de pantalla completa, que ocupa la pantalla del monitor y no tiene controles visibles.
// Establece la propiedad "PageMode" en "PdfPageMode.UseThumbs" para que el lector de PDF muestre un panel separado
// con una miniatura para cada página del documento.
// Establece la propiedad "PageMode" en "PdfPageMode.UseOC" para que el lector de PDF muestre un panel separado
// que nos permite trabajar con cualquier capa presente en el documento.
// Establece la propiedad "PageMode" en "PdfPageMode.UseOutlines" para obtener el lector de PDF
// también para mostrar el esquema, si es posible.
// Establezca la propiedad "PageMode" en "PdfPageMode.UseNone" para que el lector de PDF muestre solo el documento.
// Establece la propiedad "PageMode" en "PdfPageMode.UseAttachments" para hacer visible el panel de archivos adjuntos.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

Se muestra cómo procesar marcadores en encabezados/pies de página en un documento que estamos renderizando a PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establezca la propiedad "PageMode" en "PdfPageMode.UseOutlines" para mostrar el panel de navegación del esquema en el PDF de salida.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Establece la propiedad "DefaultBookmarksOutlineLevel" en "1" para mostrar todo
// marcadores en el primer nivel del esquema en el PDF de salida.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Establece la propiedad "HeaderFooterBookmarksExportMode" en "HeaderFooterBookmarksExportMode.None" para
// no exportar ningún marcador que esté dentro de encabezados/pies de página.
// Establece la propiedad "HeaderFooterBookmarksExportMode" en "HeaderFooterBookmarksExportMode.First" para
// solo exporta marcadores en el encabezado/pie de página de la primera sección.
// Establece la propiedad "HeaderFooterBookmarksExportMode" en "HeaderFooterBookmarksExportMode.All" para
// exporta los marcadores que están en todos los encabezados/pies de página.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Ver también

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
