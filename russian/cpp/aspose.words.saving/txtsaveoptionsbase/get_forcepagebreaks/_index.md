---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks метод"
linktitle: "get_ForcePageBreaks"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks метод. Позволяет указать, следует ли сохранять разрывы страниц при экспорте. Значение по умолчанию — false в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


Позволяет указать, следует ли сохранять разрывы страниц при экспорте. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## Примеры



Показывает, как указать, сохранять ли разрывы страниц при экспорте документа в обычный текст.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3");

// Создайте объект "TxtSaveOptions", который можно передать в метод "Save" документа
// метод для изменения способа сохранения документа в обычный текст.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Объекты Aspose.Words "Document" имеют разрывы страниц, как и документы Microsoft Word.
// Форматы сохранения, такие как ".txt", представляют собой непрерывный текст без разрывов страниц.
// Установите свойство "ForcePageBreaks" в значение "true", чтобы сохранить все разрывы страниц в виде символов '\\f'.
// Установите свойство "ForcePageBreaks" в значение "false", чтобы удалить все разрывы страниц.
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// Если мы загрузим обычный текстовый документ с разрывами страниц,
// объект "Document" использует их для разбивки тела на страницы.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## См. также

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
