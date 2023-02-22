---
title: OutlineOptions.DefaultBookmarksOutlineLevel
second_title: Referencia de API de Aspose.Words para .NET
description: OutlineOptions propiedad. Especifica el nivel predeterminado en el esquema del documento en el que se muestran los marcadores de Word.
type: docs
weight: 50
url: /es/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Especifica el nivel predeterminado en el esquema del documento en el que se muestran los marcadores de Word.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

### Observaciones

El nivel de marcadores individuales se puede especificar usando[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) propiedad.

Especifique 0 y los marcadores de Word no se mostrarán en el esquema del documento. Especifique 1 y los marcadores de Word se mostrarán en el esquema del documento en el nivel 1; 2 para el nivel 2 y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

### Ejemplos

Programas para procesar marcadores en encabezados/pies de página en un documento que estamos renderizando a PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establezca la propiedad "PageMode" en "PdfPageMode.UseOutlines" para mostrar el panel de navegación del esquema en el PDF de salida.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Establecer la propiedad "DefaultBookmarksOutlineLevel" en "1" para mostrar todo
// marcadores en el primer nivel del esquema en el PDF de salida.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Establecer la propiedad "HeaderFooterBookmarksExportMode" en "HeaderFooterBookmarksExportMode.None" para
// no exportar ningún marcador que esté dentro de los encabezados/pies de página.
// Establecer la propiedad "HeaderFooterBookmarksExportMode" en "HeaderFooterBookmarksExportMode.First" para
// exportar solo marcadores en el encabezado/pie de página de la primera sección.
// Establecer la propiedad "HeaderFooterBookmarksExportMode" en "HeaderFooterBookmarksExportMode.All" para
// exportar marcadores que están en todos los encabezados/pies de página.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Ver también

* class [OutlineOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../outlineoptions/)
* asamblea [Aspose.Words](../../../)


