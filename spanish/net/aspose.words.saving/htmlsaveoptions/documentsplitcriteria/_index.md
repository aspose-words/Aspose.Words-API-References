---
title: HtmlSaveOptions.DocumentSplitCriteria
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Especifica cómo se debe dividir el documento al guardarlo enHtml  Epub oAzw3 formato. El valor predeterminado esNone para HTML y HeadingParagraph para EPUB y AZW3.
type: docs
weight: 80
url: /es/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Especifica cómo se debe dividir el documento al guardarlo enHtml , Epub oAzw3 formato. El valor predeterminado esNone para HTML y HeadingParagraph para EPUB y AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

### Observaciones

Normalmente querrás guardar un documento en HTML como un solo archivo. Pero en algunos casos es preferible dividir la salida en varias páginas HTML más pequeñas. Al guardar en formato HTML, estas páginas se generarán en archivos o secuencias individuales. Al guardar en formato EPUB se incorporarán a los paquetes correspondientes.

Un documento no se puede dividir cuando se guarda en formato MHTML.

### Ejemplos

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
// Esto es útil para lectores que no pueden leer archivos HTML más grandes que un tamaño específico.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Especificamos que queremos exportar las propiedades del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Ver también

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


