---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad DefaultBookmarksOutlineLevel mejora sus documentos de Word al optimizar la visibilidad de los marcadores en el esquema. ¡Aumente su productividad hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Especifica el nivel predeterminado en el esquema del documento en el que se mostrarán los marcadores de Word.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Observaciones

Se puede especificar el nivel de marcadores individuales usando[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) propiedad.

Especifique 0 y los marcadores de Word no se mostrarán en el esquema del documento. Especifique 1 y los marcadores de Word se mostrarán en el esquema del documento en el nivel 1; 2 para el nivel 2 y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

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

* class [OutlineOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
