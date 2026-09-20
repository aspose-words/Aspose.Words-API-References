---
title: "Метод Aspose::Words::Font::get_Color"
linktitle: "get_Color"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Color. Получает или задает цвет шрифта в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/font/get_color/
---
## Font::get_Color method


Получает или задаёт цвет шрифта.

```cpp
System::Drawing::Color Aspose::Words::Font::get_Color()
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

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
