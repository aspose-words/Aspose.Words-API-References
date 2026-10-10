---
title: "Aspose::Words::Saving::TxtExportHeadersFootersMode enum"
linktitle: "TxtExportHeadersFootersMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtExportHeadersFootersMode enum. Anger hur sidhuvuden och sidfötter exporteras till rent textformat i C++."
type: docs
weight: 86000
url: /sv/cpp/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enum


Anger hur sidhuvuden och sidfötter exporteras till vanligt textformat.

```cpp
enum class TxtExportHeadersFootersMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Inga sidhuvuden och sidfötter exporteras. |
| PrimaryOnly | 1 | Endast primära sidhuvuden och sidfötter exporteras i början och slutet av varje avsnitt. |
| AllAtEnd | 2 | Alla sidhuvuden och sidfötter placeras efter alla avsnittskroppar i slutet av ett dokument. |


## Exempel



Visar hur man anger hur sidhuvuden och sidfötter exporteras till rent textformat.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Infoga jämna och primära sidhuvuden/sidfötter i dokumentet.
// De primära sidhuvudena/sidfötterna kommer att åsidosätta de jämna sidhuvudena/sidfötterna.
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// Infoga sidor för att visa dessa sidhuvuden och sidfötter.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Skapa ett \"TxtSaveOptions\"-objekt, som vi kan skicka till dokumentets \"Save\"-metod
// för att ändra hur vi sparar dokumentet som ren text.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Ställ in egenskapen "ExportHeadersFootersMode" till "TxtExportHeadersFootersMode.None"
// för att inte exportera några sidhuvuden/sidfötter.
// Ställ in egenskapen "ExportHeadersFootersMode" till "TxtExportHeadersFootersMode.PrimaryOnly"
// för att endast exportera primära sidhuvuden/sidfötter.
// Ställ in egenskapen "ExportHeadersFootersMode" till "TxtExportHeadersFootersMode.AllAtEnd"
// för att placera alla sidhuvuden och sidfötter för alla avsnittskroppar i slutet av dokumentet.
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

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
