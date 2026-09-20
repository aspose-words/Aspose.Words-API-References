---
title: "Enumeración Aspose::Words::Saving::TxtExportHeadersFootersMode"
linktitle: "TxtExportHeadersFootersMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Saving::TxtExportHeadersFootersMode. Especifica la forma en que los encabezados y pies de página se exportan al formato de texto plano en C++."
type: docs
weight: 86000
url: /es/cpp/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enum


Especifica la forma en que los encabezados y pies de página se exportan al formato de texto plano.

```cpp
enum class TxtExportHeadersFootersMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | No se exportan encabezados ni pies de página. |
| PrimaryOnly | 1 | Solo los encabezados y pies de página principales se exportan al inicio y al final de cada sección. |
| AllAtEnd | 2 | Todos los encabezados y pies de página se colocan después de todos los cuerpos de sección al final del documento. |


## Ejemplos



Muestra cómo especificar la exportación de encabezados y pies de página al formato de texto plano.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserte encabezados/pies de página pares y principales en el documento.
// Los encabezados/pies de página principales sobrescribirán a los pares.
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// Inserte páginas para mostrar estos encabezados y pies de página.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
// para modificar cómo guardamos el documento en texto plano.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Establezca la propiedad "ExportHeadersFootersMode" a "TxtExportHeadersFootersMode.None"
// para no exportar ningún encabezado/pie de página.
// Establezca la propiedad "ExportHeadersFootersMode" a "TxtExportHeadersFootersMode.PrimaryOnly"
// para exportar solo los encabezados/pies de página principales.
// Establezca la propiedad "ExportHeadersFootersMode" a "TxtExportHeadersFootersMode.AllAtEnd"
// para colocar todos los encabezados y pies de página de todos los cuerpos de sección al final del documento.
saveOptions->set_ExportHeadersFootersMode(txtExportHeadersFootersMode);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt");

System::String newLine = System::Environment::get_NewLine();
switch (txtExportHeadersFootersMode)
{
    case Aspose::Words::Saving::TxtExportHeadersFootersMode::AllAtEnd:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Even header{0}{1}", newLine, newLine) + System::String::Format(u"Primary header{0}{1}", newLine, newLine) + System::String::Format(u"Even footer{0}{1}", newLine, newLine) + System::String::Format(u"Primary footer{0}{1}", newLine, newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::PrimaryOnly:
        ASSERT_EQ(System::String::Format(u"Primary header{0}", newLine) + System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Primary footer{0}", newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::None:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine), docText);
        break;

}
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
