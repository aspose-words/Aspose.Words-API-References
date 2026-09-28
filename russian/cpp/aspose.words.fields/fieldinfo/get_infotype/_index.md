---
title: "Aspose::Words::Fields::FieldInfo::get_InfoType метод"
linktitle: "get_InfoType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldInfo::get_InfoType метод. Получает или задает тип свойства документа для вставки в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldinfo/get_infotype/
---
## FieldInfo::get_InfoType method


Получает или задает тип свойства документа для вставки.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_InfoType()
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
