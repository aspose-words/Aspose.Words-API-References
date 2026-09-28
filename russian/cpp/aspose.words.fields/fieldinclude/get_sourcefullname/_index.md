---
title: "Метод Aspose::Words::Fields::FieldInclude::get_SourceFullName"
linktitle: "get_SourceFullName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldInclude::get_SourceFullName. Получает или задает расположение документа в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fields/fieldinclude/get_sourcefullname/
---
## FieldInclude::get_SourceFullName method


Получает или задает расположение документа.

```cpp
System::String Aspose::Words::Fields::FieldInclude::get_SourceFullName() override
```


## Примеры



Показывает, как создать поле INCLUDE и установить его свойства.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Мы можем использовать поле INCLUDE для импорта части другого документа в локальной файловой системе.
// Закладка из другого документа, на которую мы ссылаемся этим полем, содержит импортированную часть.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## См. также

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
