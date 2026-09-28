---
title: "Перечисление Aspose::Words::Loading::DocumentDirection"
linktitle: "DocumentDirection"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Loading::DocumentDirection. Позволяет указать направление потока текста в документе на C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.loading/documentdirection/
---
## DocumentDirection enum


Позволяет указать направление потока текста в документе.

```cpp
enum class DocumentDirection
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| LeftToRight | 0 | Направление слева направо. |
| RightToLeft | 1 | Направление справа налево. |
| Авто | 2 | Автоматическое определение направления. |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
