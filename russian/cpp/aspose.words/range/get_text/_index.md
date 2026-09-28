---
title: "Метод Aspose::Words::Range::get_Text"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Range::get_Text. Получает текст диапазона в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/range/get_text/
---
## Range::get_Text method


Получает текст диапазона.

```cpp
System::String Aspose::Words::Range::get_Text()
```

## Примечания


Возвращаемая строка включает все управляющие и специальные символы, как описано в [ControlChar](../../controlchar/).

## Примеры



Показывает, как получить текстовое содержимое всех узлов, охватываемых диапазоном.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## См. также

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
