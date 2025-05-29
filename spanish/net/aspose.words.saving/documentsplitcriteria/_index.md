---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words para .NET
description: Descubra cómo Aspose.Words.Saving.DocumentSplitCriteria optimiza la división de documentos para formatos HTML, EPUB y AZW3 óptimos. ¡Optimice su proceso de guardado!
type: docs
weight: 5710
url: /es/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Especifica cómo se divide el documento en partes al guardarlo enHtml , Epub oAzw3 formato.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El documento no está dividido. |
| PageBreak | `1` | El documento se divide en partes en saltos de página explícitos. Un salto de página se puede especificar mediante un[`PageBreak`](../../aspose.words/controlchar/pagebreak/) carácter, un salto de sección que especifica el inicio de una nueva sección en una página nueva, o un párrafo que tiene su[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) propiedad establecida en`verdadero` . |
| ColumnBreak | `2` | El documento se divide en partes en los saltos de columna. Un salto de columna se puede especificar mediante un[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) carácter o un salto de sección que especifica el inicio de una nueva sección en una nueva columna. |
| SectionBreak | `4` | El documento se divide en partes en un salto de sección de cualquier tipo. |
| HeadingParagraph | `8` | El documento está dividido en partes en un párrafo formateado utilizando un estilo de encabezado**Título 1** ,**Título 2** etc. Usar junto con[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) para especificar los niveles de encabezado (desde 1 hasta el nivel especificado) en los que se dividirá. |

## Observaciones

`DocumentSplitCriteria`Es un conjunto de indicadores que se pueden combinar. Por ejemplo, se puede dividir el documento "x000d_" en saltos de página y encabezados de párrafo en la misma operación de exportación.

Diferentes criterios pueden superponerse parcialmente. Por ejemplo,**Título 1** El estilo se da frecuentemente [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) propiedad por lo que cae bajo dos criterios:PageBreak y HeadingParagraph. Algunos saltos de sección pueden provocar saltos de página, etc. En casos típicos, especificar solo un indicador es la opción más práctica.

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
