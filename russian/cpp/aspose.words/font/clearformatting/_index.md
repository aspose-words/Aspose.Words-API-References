---
title: "Метод Aspose::Words::Font::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::ClearFormatting. Сбрасывает форматирование шрифта к значениям по умолчанию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


Сбрасывает форматирование шрифта к значениям по умолчанию.

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## Примечания


Удаляет все явно заданное форматирование шрифта на объекте, из которого был получен [Font](../), чтобы форматирование шрифта наследовалось от соответствующего родителя.

## Примеры



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
