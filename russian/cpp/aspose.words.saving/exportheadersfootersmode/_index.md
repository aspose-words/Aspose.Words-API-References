---
title: "Перечисление Aspose::Words::Saving::ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Saving::ExportHeadersFootersMode. Указывает, как заголовки и колонтитулы экспортируются в HTML, MHTML или EPUB в C++."
type: docs
weight: 55000
url: /ru/cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


Указывает, как заголовки и колонтитулы экспортируются в HTML, MHTML или EPUB.

```cpp
enum class ExportHeadersFootersMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Заголовки и колонтитулы не экспортируются. |
| PerSection | 1 | Основные колонтитулы экспортируются в начале и в конце каждого раздела. |
| FirstSectionHeaderLastSectionFooter | 2 | Основной колонтитул первого раздела экспортируется в начале документа, а основной нижний колонтитул — в конце. |
| FirstPageHeaderFooterPerSection | 3 | Колонтитулы первой страницы экспортируются в начале и в конце каждого раздела. |


## Примеры



Показывает, как исключить колонтитулы при сохранении документа в HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Этот документ содержит колонтитулы. Мы можем получить к ним доступ через коллекцию "HeadersFooters".
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// Форматы, такие как .html, не разбивают документ на страницы, поэтому колонтитулы не будут работать так же.
// как это происходит, когда мы открываем документ как .docx в Microsoft Word.
// Если мы конвертируем документ с колонтитулами в html, преобразование включит колонтитулы в основной текст.
// Мы можем использовать объект SaveOptions, чтобы исключить колонтитулы при конвертации в html.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// Откройте сохранённый документ и убедитесь, что он не содержит текст колонтитула.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
