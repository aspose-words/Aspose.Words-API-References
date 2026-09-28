---
title: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath метод"
linktitle: "get_IncludeFullPath"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath метод. Получает или задает, следует ли включать полное имя пути к файлу, в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


Получает или задает, следует ли включать полное имя пути к файлу.

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


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

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
