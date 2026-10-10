---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode metodo"
linktitle: "get_ExportHeadersFootersMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode metodo. Specifica il modo in cui intestazioni e piè di pagina vengono esportati nei formati di testo. Il valore predefinito è PrimaryOnly in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/txtsaveoptionsbase/get_exportheadersfootersmode/
---
## TxtSaveOptionsBase::get_ExportHeadersFootersMode method


Specifica il modo in cui intestazioni e piè di pagina vengono esportati nei formati di testo. Il valore predefinito è [PrimaryOnly](../../txtexportheadersfootersmode/).

```cpp
Aspose::Words::Saving::TxtExportHeadersFootersMode Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode() const
```


## Esempi



Mostra come specificare come esportare intestazioni e piè di pagina nel formato di testo semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserisci intestazioni/piè di pagina pari e primari nel documento.
// Le intestazioni/piè di pagina primari sovrascriveranno le intestazioni/piè di pagina pari.
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// Inserisci pagine per visualizzare queste intestazioni e piè di pagina.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo semplice.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Imposta la proprietà "ExportHeadersFootersMode" a "TxtExportHeadersFootersMode.None"
// per non esportare alcuna intestazione/piè di pagina.
// Imposta la proprietà "ExportHeadersFootersMode" a "TxtExportHeadersFootersMode.PrimaryOnly"
// per esportare solo le intestazioni/piè di pagina primari.
// Imposta la proprietà "ExportHeadersFootersMode" a "TxtExportHeadersFootersMode.AllAtEnd"
// per posizionare tutte le intestazioni e i piè di pagina per tutti i corpi di sezione alla fine del documento.
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

## Vedi anche

* Enum [TxtExportHeadersFootersMode](../../txtexportheadersfootersmode/)
* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
