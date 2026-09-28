---
title: "Метод Aspose::Words::Font::get_LocaleId"
linktitle: "get_LocaleId"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_LocaleId. Получает или задает идентификатор локали (язык) отформатированных символов в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words/font/get_localeid/
---
## Font::get_LocaleId method


Получает или задаёт идентификатор локали (язык) отформатированных символов.

```cpp
int32_t Aspose::Words::Font::get_LocaleId()
```


## Примеры



Показывает, как установить локаль текста, который мы добавляем с помощью DocumentBuilder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Если мы задаем локаль шрифта как английскую и вставляем русский текст,
// английская проверка орфографии не распознает текст и отметит его как ошибку.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());
builder->Writeln(u"Привет!");

// Установите соответствующую локаль для текста, который собираемся добавить, чтобы применить нужную проверку орфографии.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU", false)->get_LCID());
builder->Writeln(u"Привет!");

doc->Save(get_ArtifactsDir() + u"Font.LocaleId.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
