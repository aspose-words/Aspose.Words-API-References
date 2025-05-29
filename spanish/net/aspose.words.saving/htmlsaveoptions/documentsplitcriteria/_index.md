---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words para .NET
description: Descubra la propiedad DocumentSplitCriteria de HtmlSaveOptions para optimizar el guardado de documentos en formatos HTML, EPUB y AZW3. ¡Mejore su control de formato hoy mismo!
type: docs
weight: 80
url: /es/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Especifica cómo se debe dividir el documento al guardarlo enHtml , Epub oAzw3 format. El valor predeterminado esNone para HTML y HeadingParagraph para EPUB y AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Observaciones

Normalmente, usted querría guardar un documento en HTML como un solo archivo. Pero en algunos casos es preferible dividir la salida en varias páginas HTML más pequeñas. Al guardar en formato HTML, estas páginas se exportarán a archivos o secuencias individuales. Al guardar en formato EPUB, se incorporarán a los paquetes correspondientes.

No se puede dividir un documento al guardarlo en formato MHTML.

## Ejemplos

Muestra cómo utilizar una codificación específica al guardar un documento en .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilice un objeto SaveOptions para especificar la codificación de un documento que guardaremos.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// De forma predeterminada, un documento .epub de salida tendrá todo su contenido en una parte HTML.
// Un criterio de división nos permite segmentar el documento en varias partes HTML.
// Estableceremos los criterios para dividir el documento en párrafos de encabezado.
// Esto es útil para los lectores que no pueden leer archivos HTML más grandes que un tamaño específico.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Especificamos que queremos exportar las propiedades del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Ver también

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
