---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode método"
linktitle: "get_ExportHeadersFootersMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode método. Especifica cómo se exportan los encabezados y pies de página a HTML, MHTML o EPUB. El valor predeterminado es PerSection para HTML/MHTML y None para EPUB en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


Especifica cómo se exportan los encabezados y pies de página a HTML, MHTML o EPUB. El valor predeterminado es [PerSection](../../exportheadersfootersmode/) para HTML/MHTML y [None](../../exportheadersfootersmode/) para EPUB.

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## Observaciones


Es difícil exportar de manera significativa los encabezados y pies de página a HTML porque HTML no está paginado.

Cuando esta propiedad es [PerSection](../../exportheadersfootersmode/), Aspose.Words exporta solo los encabezados y pies de página principales al inicio y al final de cada sección.

Cuando es [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/) solo se exportan el primer encabezado principal y el último pie de página principal (incluyendo los vinculados al anterior).

Puede desactivar la exportación de encabezados y pies de página por completo estableciendo esta propiedad a [None](../../exportheadersfootersmode/).

## Ejemplos



Muestra cómo omitir encabezados/pies de página al guardar un documento en HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Este documento contiene encabezados y pies de página. Podemos acceder a ellos a través de la colección "HeadersFooters".
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// Los formatos como .html no dividen el documento en páginas, por lo que los encabezados/pies de página no funcionarán de la misma manera
// como lo harían al abrir el documento como .docx usando Microsoft Word.
// Si convertimos un documento con encabezados/pies de página a html, la conversión incorporará los encabezados/pies de página al texto del cuerpo.
// Podemos usar un objeto SaveOptions para omitir encabezados/pies de página mientras convertimos a html.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// Abra nuestro documento guardado y verifique que no contenga el texto del encabezado
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## Ver también

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
