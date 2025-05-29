---
title: HeaderFooterBookmarksExportMode Enum
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words para .NET
description: Descubra cómo Aspose.Words.Saving.HeaderFooterBookmarksExportMode mejora la exportación de marcadores en encabezados y pies de página para una gestión perfecta de documentos.
type: docs
weight: 5800
url: /es/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Especifica cómo se exportan los marcadores en encabezados y pies de página.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Los marcadores en encabezados/pies de página no se exportan. |
| First | `1` | Solo se exporta el marcador en el primer encabezado/pie de página de la sección. |
| All | `2` | Se exportan los marcadores en todos los encabezados y pies de página. |

## Ejemplos

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
