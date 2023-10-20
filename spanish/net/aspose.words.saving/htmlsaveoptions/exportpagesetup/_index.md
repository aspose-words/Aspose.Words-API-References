---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: Aspose.Words para .NET
description: HtmlSaveOptions ExportPageSetup propiedad. Especifica si la configuración de la página se exporta a HTML MHTML o EPUB. El valor predeterminado esFALSO  en C#.
type: docs
weight: 220
url: /es/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Especifica si la configuración de la página se exporta a HTML, MHTML o EPUB. El valor predeterminado es`FALSO` .

```csharp
public bool ExportPageSetup { get; set; }
```

## Observaciones

Cada[`Section`](../../../aspose.words/section/) en el modelo de documento Aspose.Words proporciona información de configuración de página a través de[`PageSetup`](../../../aspose.words/pagesetup/) clase. Cuando exporta un documento a formato HTML, es posible que necesite conservar esta información para su uso posterior. En particular, la configuración de la página puede ser importante para la representación en medios paginados (impresión) o la conversión posterior a los formatos de archivo nativos de Microsoft Word (DOCX, DOC, RTF, WML).

En la mayoría de los casos, HTML está pensado para visualizarse en navegadores donde no se realiza la paginación. Entonces esta característica está inactiva de forma predeterminada.

## Ejemplos

Muestra cómo decidir si se conserva la estructura de la sección/la información de configuración de la página al guardar en HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TopMargin = 36.0;
pageSetup.BottomMargin = 36.0;
pageSetup.PaperSize = PaperSize.A5;

// Al guardar el documento en HTML, podemos pasar un objeto SaveOptions
// para decidir si preservar o descartar la configuración de configuración de la página.
// Si configuramos el indicador "ExportPageSetup" en "verdadero", el documento HTML de salida contendrá nuestra configuración de configuración de página.
// Si configuramos el indicador "ExportPageSetup" en "falso", la operación de guardar descartará nuestra configuración de configuración de página
// para la primera sección, y ambas secciones se verán idénticas.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.True(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" +
        "</style>"));

    Assert.True(outDocContents.Contains(
        "<div class=\"Section_1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));

    Assert.True(outDocContents.Contains(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
