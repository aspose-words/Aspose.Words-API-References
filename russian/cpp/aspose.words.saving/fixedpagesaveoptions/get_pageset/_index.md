---
title: "Метод Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet"
linktitle: "get_PageSet"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet. Получает или задает страницы для рендеринга. По умолчанию — все страницы документа в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


Получает или задает страницы для рендеринга. По умолчанию — все страницы документа.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## Примеры



Показывает, как извлекать страницы по точным индексам страниц.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте пять страниц в документ.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Создайте объект "XpsSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Используйте свойство "PageSet", чтобы выбрать набор страниц документа для сохранения в выходной XPS.
// В этом случае мы выберем, используя нулевой индекс, только три страницы: страницу 1, страницу 2 и страницу 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## См. также

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
