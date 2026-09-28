---
title: "Aspose::Words::Fields::FieldKeywords::get_Text метод"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldKeywords::get_Text метод. Получает или задаёт текст ключевых слов в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


Получает или задаёт текст ключевых слов.

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## Примеры



Показывает, как вставить поле KEYWORDS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add some keywords, also referred to as \"теги\" in File Explorer.
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// Поле KEYWORDS отображает значение этого свойства.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// Установка значения свойства Text поля,
// а затем обновление поля также перезапишет соответствующее встроенное свойство новым значением.
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## См. также

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
