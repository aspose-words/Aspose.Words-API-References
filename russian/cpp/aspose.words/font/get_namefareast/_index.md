---
title: "Метод Aspose::Words::Font::get_NameFarEast"
linktitle: "get_NameFarEast"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_NameFarEast. Возвращает или задает название восточноазиатского шрифта в C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words/font/get_namefareast/
---
## Font::get_NameFarEast method


Возвращает или задаёт название восточноазиатского шрифта.

```cpp
System::String Aspose::Words::Font::get_NameFarEast()
```


## Примеры



Показывает, как вставлять и форматировать текст на языке Дальнего Востока.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Укажите настройки шрифта, которые построитель документа применит к любому вставляемому тексту.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Назовите эквиваленты "FarEast" для нашего шрифта и локали.
// Если построитель вставляет азиатские символы с этой конфигурацией шрифта, то каждый фрагмент, содержащий
// эти символы будут отображаться с использованием шрифта/локали "FarEast" вместо значения по умолчанию.
// Это может быть полезно, когда западный шрифт не имеет идеального отображения азиатских символов.
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// Этот текст будет отображаться в шрифте/локали по умолчанию.
builder->Writeln(u"Hello world!");

// Поскольку это азиатские символы, этот фрагмент применит наши эквиваленты шрифта/локали "FarEast".
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
