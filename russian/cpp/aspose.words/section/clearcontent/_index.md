---
title: "Aspose::Words::Section::ClearContent метод"
linktitle: "ClearContent"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Section::ClearContent метод. Очищает раздел в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


Очищает раздел.

```cpp
void Aspose::Words::Section::ClearContent()
```

## Примечания


Текст [Body](../get_body/) очищается, остаётся только один пустой абзац, представляющий разрыв раздела.

Текст всех колонтитулов очищается, но объекты [HeaderFooter](../../headerfooter/) сами не удаляются.

## Примеры



Показывает, как очистить содержимое раздела.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Выполнение метода "ClearContent" удалит всё содержимое раздела
// но оставит пустой абзац, чтобы снова добавить содержимое.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## См. также

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
