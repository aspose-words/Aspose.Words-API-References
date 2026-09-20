---
title: "Метод Aspose::Words::Font::get_Bold"
linktitle: "get_Bold"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Bold. Истина, если шрифт отформатирован полужирным в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


True, если шрифт оформлен как полужирный.

```cpp
bool Aspose::Words::Font::get_Bold()
```


## Примеры



Показывает, как вставить отформатированный текст с помощью [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Укажите форматирование шрифта, затем добавьте текст.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
