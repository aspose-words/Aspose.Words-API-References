---
title: "Aspose::Words::Fields::FieldComments::get_Text метод"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldComments::get_Text метод. Получает или задает текст комментариев в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


Получает или задает текст комментариев.

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## Примеры



Показывает, как использовать поле COMMENTS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите значение встроенного свойства документа "Comments".
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// Создайте поле COMMENTS, чтобы отобразить значение этого встроенного свойства.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// Если мы зададим значение свойства Text поля COMMENTS и обновим его, поле будет
// перезаписывать текущее значение встроенного свойства "Comments" значением его свойства Text,
// а затем отображать новое значение.
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## См. также

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
