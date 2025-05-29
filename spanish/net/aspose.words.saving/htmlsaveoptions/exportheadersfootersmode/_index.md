---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlSaveOptions ExportHeadersFootersMode optimiza la salida de encabezados y pies de página en formatos HTML, MHTML y EPUB. ¡Optimice la presentación de su documento!
type: docs
weight: 160
url: /es/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Especifica cómo se envían los encabezados y pies de página a HTML, MHTML o EPUB. El valor predeterminado esPerSection para HTML/MHTML yNone para EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## Observaciones

Es difícil generar encabezados y pies de página de forma significativa en HTML porque el HTML no está paginado.

Cuando esta propiedad esPerSectionAspose.Words exporta solo encabezados y pies de página principales al principio y al final de cada sección.

Cuando lo esFirstSectionHeaderLastSectionFooter solo se exportan el primer encabezado principal y el último pie de página principal (incluidos los vinculados al anterior).

Puede deshabilitar la exportación de encabezados y pies de página por completo configurando esta propiedad enNone.

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

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
