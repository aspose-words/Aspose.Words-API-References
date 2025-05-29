---
title: PdfPageMode Enum
linktitle: PdfPageMode
articleTitle: PdfPageMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.PdfPageMode para personalizar las opciones de visualización de PDF y mejorar la experiencia del usuario en cualquier lector de PDF. ¡Optimice sus documentos hoy mismo!
type: docs
weight: 6300
url: /es/net/aspose.words.saving/pdfpagemode/
---
## PdfPageMode enumeration

Especifica cómo debe mostrarse el documento PDF cuando se abre en el lector de PDF.

```csharp
public enum PdfPageMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| UseNone | `0` | Ni el contorno del documento ni las imágenes en miniatura son visibles. |
| UseOutlines | `1` | El contorno del documento es visible. Tenga en cuenta que si no hay contornos en el documento PDF, el panel de navegación de contornos no será visible de todos modos. |
| UseThumbs | `2` | Las imágenes en miniatura son visibles. |
| FullScreen | `3` | Modo de pantalla completa, sin barra de menú, controles de ventana ni ninguna otra ventana visible. |
| UseOC | `4` | El panel de grupo de contenido opcional está visible. |
| UseAttachments | `5` | El panel de archivos adjuntos está visible. |

## Ejemplos

Muestra cómo establecer instrucciones que algunos lectores de PDF deben seguir al abrir un documento de salida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establezca la propiedad "PageMode" en "PdfPageMode.FullScreen" para que el lector de PDF abra el archivo guardado.
// documento en modo de pantalla completa, que ocupa la pantalla del monitor y no tiene controles visibles.
// Establezca la propiedad "PageMode" en "PdfPageMode.UseThumbs" para que el lector de PDF muestre un panel separado
// con una miniatura para cada página del documento.
// Establezca la propiedad "PageMode" en "PdfPageMode.UseOC" para que el lector de PDF muestre un panel separado
// que nos permite trabajar con cualquier capa presente en el documento.
// Establezca la propiedad "PageMode" en "PdfPageMode.UseOutlines" para obtener el lector de PDF
// también para mostrar el contorno, si es posible.
// Establezca la propiedad "PageMode" en "PdfPageMode.UseNone" para que el lector de PDF muestre solo el documento en sí.
// Establezca la propiedad "PageMode" en "PdfPageMode.UseAttachments" para hacer visible el panel de archivos adjuntos.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

Muestra cómo procesar marcadores en encabezados y pies de página en un documento que estamos convirtiendo a PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establezca la propiedad "PageMode" en "PdfPageMode.UseOutlines" para mostrar el panel de navegación de esquema en el PDF de salida.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Establezca la propiedad "DefaultBookmarksOutlineLevel" en "1" para mostrar todos
// marcadores en el primer nivel del esquema en el PDF de salida.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Establezca la propiedad "HeaderFooterBookmarksExportMode" en "HeaderFooterBookmarksExportMode.None" para
// no exportar ningún marcador que esté dentro de encabezados/pies de página.
// Establezca la propiedad "HeaderFooterBookmarksExportMode" en "HeaderFooterBookmarksExportMode.First" para
// solo exporta marcadores en el encabezado/pie de página de la primera sección.
// Establezca la propiedad "HeaderFooterBookmarksExportMode" en "HeaderFooterBookmarksExportMode.All" para
// exportar marcadores que están en todos los encabezados/pies de página.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
