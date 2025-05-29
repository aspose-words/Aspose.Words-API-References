---
title: OutlineOptions Class
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.OutlineOptions para personalizar la configuración del esquema de su documento para una mejor organización y claridad.
type: docs
weight: 6140
url: /es/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

Permite especificar opciones de contorno.

Para obtener más información, visite el[Guardar un documento](https://docs.aspose.com/words/net/save-a-document/) Artículo de documentación.

```csharp
public class OutlineOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [OutlineOptions](outlineoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BookmarksOutlineLevels](../../aspose.words.saving/outlineoptions/bookmarksoutlinelevels/) { get; } | Permite especificar el nivel de esquema de marcadores individuales. |
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | Obtiene o establece un valor que determina si se deben crear o no niveles de contorno faltantes cuando se exporta el documento. |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | Especifica si se deben crear o no esquemas para encabezados (párrafos formateados con los estilos de encabezado) dentro de las tablas. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | Especifica el nivel predeterminado en el esquema del documento en el que se mostrarán los marcadores de Word. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | Especifica cuántos niveles del esquema del documento se mostrarán expandidos cuando se visualice el archivo. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | Especifica cuántos niveles de encabezados (párrafos formateados con los estilos de encabezado) se incluirán en el esquema del documento. |

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
