---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup"
linktitle: "get_ExportPageSetup"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup. Especifica si la configuración de página se exporta a HTML, MHTML o EPUB. El valor predeterminado es false en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


Especifica si la configuración de página se exporta a HTML, MHTML o EPUB. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## Observaciones


Cada [Section](../../../aspose.words/section/) en el modelo de documento de Aspose.Words proporciona información de configuración de página a través de la clase [PageSetup](../../../aspose.words/pagesetup/). Cuando exportas un documento al formato HTML puede que necesites conservar esta información para su uso posterior. En particular, la configuración de página puede ser importante para la renderización en medios paginados (impresión) o la conversión subsecuente a los formatos nativos de Microsoft Word (DOCX, DOC, RTF, WML).

En la mayoría de los casos, HTML está destinado a visualizarse en navegadores donde no se realiza paginación. Por lo tanto, esta característica está inactiva por defecto.

## Ejemplos



Muestra cómo decidir si se conserva la información de la estructura de secciones/configuración de página al guardar en HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TopMargin(36.0);
pageSetup->set_BottomMargin(36.0);
pageSetup->set_PaperSize(Aspose::Words::PaperSize::A5);

// Al guardar el documento en HTML, podemos pasar un objeto SaveOptions
// para decidir si conservar o descartar la configuración de página.
// Si establecemos la bandera "ExportPageSetup" a "true", el documento HTML de salida contendrá nuestra configuración de página.
// Si establecemos la bandera "ExportPageSetup" a "false", la operación de guardado descartará nuestra configuración de página
// para la primera sección, y ambas secciones se verán idénticas.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageSetup(exportPageSetup);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<style type=\"text/css\">") + u"@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" + u"</style>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div class=\"Section_1\">") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div>") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
