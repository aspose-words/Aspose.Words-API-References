---
title: "Метод Aspose::Words::Style::get_BuiltIn"
linktitle: "get_BuiltIn"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Style::get_BuiltIn. True, если этот стиль является одним из встроенных стилей в MS Word в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


True, если этот стиль является одним из встроенных стилей в MS Word.

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## Примеры



Показывает, как различать пользовательские стили и встроенные стили.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Когда мы создаём документ с помощью Microsoft Word или программно, используя Aspose.Words,
// документ будет содержать набор стилей, которые можно применять к его тексту для изменения внешнего вида.
// Мы можем получить доступ к этим встроенным стилям через коллекцию "Styles" документа.
// У всех этих стилей будет установлен флаг "BuiltIn" со значением "true".
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// Создайте пользовательский стиль и добавьте его в коллекцию.
// У пользовательских стилей, подобных этому, будет установлен флаг "BuiltIn" со значением "false".
style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## См. также

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
