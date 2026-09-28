---
title: "Метод Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries"
linktitle: "get_DoNotDisplayPageBoundaries"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries. Отключает отображение пространства между верхом текста и верхним краем страницы в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.settings/viewoptions/get_donotdisplaypageboundaries/
---
## ViewOptions::get_DoNotDisplayPageBoundaries method


Отключает отображение пространства между верхом текста и верхним краем страницы.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries() const
```


## Примеры



Показывает, как скрыть вертикальные пробелы и колонтитулы в параметрах просмотра.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте содержимое, охватывающее 3 страницы.
builder->Writeln(u"Paragraph 1, Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 2, Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 3, Page 3.");

// Вставьте верхний и нижний колонтитулы.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the footer.");

// Этот документ содержит небольшое количество содержимого, которое занимает несколько полных страниц.
// Установите флаг "DoNotDisplayPageBoundaries" в "true", чтобы более старые версии Microsoft Word не отображали заголовки,
// нижние колонтитулы и большую часть вертикальных пробелов при отображении нашего документа.
// Установите флаг "DoNotDisplayPageBoundaries" в "false", чтобы более старые версии Microsoft Word
// обычно отображали наш документ.
doc->get_ViewOptions()->set_DoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayPageBoundaries.doc");
```

## См. также

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
