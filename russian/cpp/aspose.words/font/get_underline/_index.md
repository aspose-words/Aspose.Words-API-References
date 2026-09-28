---
title: "Метод Aspose::Words::Font::get_Underline"
linktitle: "get_Underline"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Underline. Получает или задает тип подчеркивания, применяемый к шрифту, в C++."
type: docs
weight: 55000
url: /ru/cpp/aspose.words/font/get_underline/
---
## Font::get_Underline method


Получает или задает тип подчеркивания, применяемого к шрифту.

```cpp
Aspose::Words::Underline Aspose::Words::Font::get_Underline()
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


Показывает, как вставить поле гиперссылки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Вставьте гиперссылку и выделите её с помощью пользовательского форматирования.
// Гиперссылка будет кликабельным фрагментом текста, который перенаправит нас к месту, указанному в URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + щелчок левой кнопкой мыши по ссылке в тексте в Microsoft Word откроет URL в новом окне веб‑браузера.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


Показывает, как настроить стиль и цвет подчеркивания текста.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## См. также

* Enum [Underline](../../underline/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
