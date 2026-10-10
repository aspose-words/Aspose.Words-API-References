---
title: "Enumeración Aspose::Words::Saving::ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Saving::ExportHeadersFootersMode. Especifica cómo se exportan los encabezados y pies de página a HTML, MHTML o EPUB en C++."
type: docs
weight: 55000
url: /es/cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


Especifica cómo se exportan los encabezados y pies de página a HTML, MHTML o EPUB.

```cpp
enum class ExportHeadersFootersMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | Los encabezados y pies de página no se exportan. |
| PerSection | 1 | Los encabezados y pies de página principales se exportan al principio y al final de cada sección. |
| FirstSectionHeaderLastSectionFooter | 2 | El encabezado principal de la primera sección se exporta al principio del documento y el pie de página principal al final. |
| FirstPageHeaderFooterPerSection | 3 | El encabezado y pie de página de la primera página se exportan al principio y al final de cada sección. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
