---
title: "Метод Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection"
linktitle: "get_DocumentDirection"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection. Получает или задает направление документа. Значение по умолчанию — LeftToRight в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.loading/txtloadoptions/get_documentdirection/
---
## TxtLoadOptions::get_DocumentDirection method


Получает или задает направление документа. Значение по умолчанию — [LeftToRight](../../documentdirection/).

```cpp
Aspose::Words::Loading::DocumentDirection Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection() const
```


## Примеры



Показывает, как определить направление текста в простом документе.
```cpp
// Создайте объект "TxtLoadOptions", который можно передать конструктору документа
// чтобы изменить способ загрузки простого документа.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Установите свойство "DocumentDirection" в "DocumentDirection.Auto" для автоматического определения
// направления каждого абзаца текста, который Aspose.Words загружает из простого текста.
// Свойство "Bidi" каждого абзаца будет хранить его направление.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Определять иврит как направление справа налево.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Определять английский как направление справа налево.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## См. также

* Enum [DocumentDirection](../../documentdirection/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
