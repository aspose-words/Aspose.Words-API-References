---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode метод"
linktitle: "get_ExportHeadersFootersMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode метод. Указывает, как заголовки и колонтитулы выводятся в HTML, MHTML или EPUB. Значение по умолчанию — PerSection для HTML/MHTML и None для EPUB в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


Указывает, как заголовки и колонтитулы выводятся в HTML, MHTML или EPUB. Значение по умолчанию — [PerSection](../../exportheadersfootersmode/) для HTML/MHTML и [None](../../exportheadersfootersmode/) для EPUB.

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## Примечания


Трудно осмысленно выводить заголовки и колонтитулы в HTML, потому что HTML не имеет разбиения на страницы.

Когда это свойство имеет значение [PerSection](../../exportheadersfootersmode/), Aspose.Words экспортирует только основные заголовки и колонтитулы в начале и в конце каждого раздела.

Когда оно равно [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/), экспортируются только первый основной заголовок и последний основной колонтитул (включая связанные с предыдущим).

Вы можете полностью отключить экспорт заголовков и колонтитулов, установив это свойство в значение [None](../../exportheadersfootersmode/).

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

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
