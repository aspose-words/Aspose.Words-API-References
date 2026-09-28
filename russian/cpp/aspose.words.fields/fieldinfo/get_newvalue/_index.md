---
title: "метод Aspose::Words::Fields::FieldInfo::get_NewValue"
linktitle: "get_NewValue"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Fields::FieldInfo::get_NewValue. Получает или задает необязательное значение, которое обновляет свойство в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fields/fieldinfo/get_newvalue/
---
## FieldInfo::get_NewValue method


Получает или задает необязательное значение, которое обновляет свойство.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_NewValue()
```


## Примеры



Показывает, как работать с полями INFO.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите значение для встроенного свойства "Comments", а затем вставьте поле INFO, чтобы отобразить значение этого свойства.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// Установка значения свойства NewValue поля и обновление
// поле также перезапишет соответствующее встроенное свойство новым значением.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## См. также

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
