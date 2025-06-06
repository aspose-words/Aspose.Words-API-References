---
title: ExportHeadersFootersMode Enum
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words ExportHeadersFootersMode para exportar encabezados y pies de página HTML, MHTML o EPUB sin problemas. ¡Optimice la conversión de sus documentos hoy mismo!
type: docs
weight: 5750
url: /es/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Especifica cómo se exportan los encabezados y pies de página a HTML, MHTML o EPUB.

```csharp
public enum ExportHeadersFootersMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Los encabezados y pies de página no se exportan. |
| PerSection | `1` | Los encabezados y pies de página principales se exportan al principio y al final de cada sección. |
| FirstSectionHeaderLastSectionFooter | `2` | El encabezado principal de la primera sección se exporta al principio del documento y el pie de página principal se encuentra al final. |
| FirstPageHeaderFooterPerSection | `3` | El encabezado y pie de página de la primera página se exportan al principio y al final de cada sección. |

## Ejemplos

Muestra cómo omitir encabezados y pies de página al guardar un documento en HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

Este documento contiene encabezados y pies de página. Podemos acceder a ellos mediante la colección "HeadersFooters".
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Los formatos como .html no dividen el documento en páginas, por lo que los encabezados y pies de página no funcionarán de la misma manera
// Lo harían cuando abrimos el documento como .docx usando Microsoft Word.
// Si convertimos un documento con encabezados/pies de página a html, la conversión asimilará los encabezados/pies de página al texto del cuerpo.
// Podemos usar un objeto SaveOptions para omitir encabezados/pies de página al convertir a HTML.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

//Abrimos nuestro documento guardado y verificamos que no contenga el texto del encabezado
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Ver también

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
