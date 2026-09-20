---
title: "Aspose::Words::Saving::TxtExportHeadersFootersMode перечисление"
linktitle: "TxtExportHeadersFootersMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::TxtExportHeadersFootersMode перечисление. Указывает способ экспорта заголовков и колонтитулов в формат простого текста в C++."
type: docs
weight: 86000
url: /ru/cpp/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enum


Указывает способ экспорта заголовков и нижних колонтитулов в формат простого текста.

```cpp
enum class TxtExportHeadersFootersMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Заголовки и колонтитулы не экспортируются. |
| PrimaryOnly | 1 | Только основные заголовки и колонтитулы экспортируются в начале и в конце каждого раздела. |
| AllAtEnd | 2 | Все заголовки и колонтитулы размещаются после всех тел разделов в самом конце документа. |


## Примеры



Показывает, как указать способ экспорта заголовков и колонтитулов в формат простого текста.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Вставьте четные и основные заголовки/колонтитулы в документ.
// Основные заголовки/колонтитулы переопределят четные заголовки/колонтитулы.
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// Вставьте страницы для отображения этих заголовков и колонтитулов.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ сохранения документа в простой текст.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Установите свойство "ExportHeadersFootersMode" в "TxtExportHeadersFootersMode.None"
// чтобы не экспортировать любые заголовки/колонтитулы.
// Установите свойство "ExportHeadersFootersMode" в "TxtExportHeadersFootersMode.PrimaryOnly"
// чтобы экспортировать только основные заголовки/колонтитулы.
// Установите свойство "ExportHeadersFootersMode" в "TxtExportHeadersFootersMode.AllAtEnd"
// разместить все колонтитулы для всех тел разделов в конце документа.
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

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
