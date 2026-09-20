---
title: "Метод Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel"
linktitle: "get_CaptionlessTableOfFiguresLabel"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel. Получает или задает имя идентификатора последовательности, используемого при построении списка иллюстраций, который не включает метку и номер подписи в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


Получает или задает имя идентификатора последовательности, используемого при построении списка иллюстраций, который не включает метку и номер подписи.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## Примеры



Показывает, как задать имя идентификатора последовательности.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## См. также

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
