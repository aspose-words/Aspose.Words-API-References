---
title: "Aspose::Words::ImportFormatOptions::get_ResolveThemeColors метод"
linktitle: "get_ResolveThemeColors"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ImportFormatOptions::get_ResolveThemeColors. Получает или задает логическое значение, которое указывает, следует ли принудительно разрешать цвета темы фигур. Значение по умолчанию — false в C++."
type: docs
weight: 8500
url: /ru/cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


Получает или задает логическое значение, которое указывает, следует ли принудительно разрешать темы цветов фигур. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## Примечания


Обратите внимание, что эта опция актуальна только для режима [KeepSourceFormatting](../../importformatmode/).

Обычно Aspose.Words не разрешает цвета темы источника при импорте, если стили могут быть сохранены без преобразования атрибутов форматирования в прямые. Однако в этом случае фактические цвета импортированных фигур могут отличаться от тех, что были в исходном документе. Причина этого — различие цветов темы в исходном и целевом документах. Установка этой опции в значение **true** принудительно разрешает цвета темы фигур источника и, следовательно, сохраняет их фактический цвет в исходном документе.

## Примеры



Показывает, как импортировать узел с разрешением исходных цветовых тем фигур.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Перейдите к основному нижнему колонтитулу и вставьте форму, использующую цвета темы.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Импортируйте исходный нижний колонтитул в целевой документ с разрешёнными цветами темы,
// чтобы форма сохраняла свой фактический цвет из исходного документа.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## См. также

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
