---
title: "Метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding"
linktitle: "get_Encoding"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding. Указывает кодировку, используемую при экспорте в HTML. Значение по умолчанию — new UTF8Encoding(true) (UTF-8 с BOM) в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


Указывает кодировку, используемую при экспорте в HTML. Значение по умолчанию — **new UTF8Encoding(true)** (UTF-8 с BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## Примеры



Показывает, как задать кодировку, используемую при экспорте документа в HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// Кодировка по умолчанию — UTF-8. Если мы хотим представить наш документ с использованием другой кодировки,
// мы можем использовать объект SaveOptions, чтобы задать конкретную кодировку.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## См. также

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
