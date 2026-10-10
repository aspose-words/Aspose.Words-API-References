---
title: "Aspose::Words::Fields::FieldOptions::get_TemplateName yöntemi."
linktitle: "get_TemplateName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldOptions::get_TemplateName yöntemi. C++'ta belge tarafından kullanılan şablonun dosya adını alır veya ayarlar."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.fields/fieldoptions/get_templatename/
---
## FieldOptions::get_TemplateName method


Belge tarafından kullanılan şablonun dosya adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_TemplateName() const
```

## Açıklamalar


Bu özellik, [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/) özelliği boşsa [FieldTemplate](../../fieldtemplate/) alanı tarafından kullanılır.

Bu özellik boşsa, varsayılan şablon dosya adı **Normal.dotm** kullanılır.

## Örnekler



Bir TEMPLATE alanını kullanarak bir belgenin şablonunun yerel dosya sistemi konumunu nasıl görüntüleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Alanları kullanarak bir şablon adı ayarlayabiliriz. Bu özellik, "doc.AttachedTemplate" boş olduğunda kullanılır.
// Bu özellik boş ise, varsayılan şablon dosya adı "Normal.dotm" kullanılır.
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

## Ayrıca Bakınız

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
