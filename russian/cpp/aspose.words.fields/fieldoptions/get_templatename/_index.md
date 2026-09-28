---
title: "Метод Aspose::Words::Fields::FieldOptions::get_TemplateName"
linktitle: "get_TemplateName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldOptions::get_TemplateName. Получает или задает имя файла шаблона, используемого документом, в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.fields/fieldoptions/get_templatename/
---
## FieldOptions::get_TemplateName method


Получает или задает имя файла шаблона, используемого документом.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_TemplateName() const
```

## Примечания


Это свойство используется полем [FieldTemplate](../../fieldtemplate/), если свойство [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/) пусто.

Если это свойство пусто, используется имя файла шаблона по умолчанию **Normal.dotm**.

## Примеры



Показывает, как использовать поле TEMPLATE для отображения локального пути к шаблону документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Мы можем задать имя шаблона с помощью полей. Это свойство используется, когда "doc.AttachedTemplate" пусто.
// Если это свойство пусто, используется имя файла шаблона по умолчанию "Normal.dotm".
doc->get_FieldOptions()->set_TemplateName(System::String::Empty);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
ASSERT_EQ(u" TEMPLATE ", field->GetFieldCode());

builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
field->set_IncludeFullPath(true);

ASSERT_EQ(u" TEMPLATE  \\p", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TEMPLATE.docx");
```

## См. также

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
