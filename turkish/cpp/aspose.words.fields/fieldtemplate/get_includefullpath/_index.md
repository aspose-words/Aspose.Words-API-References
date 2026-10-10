---
title: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath metodu"
linktitle: "get_IncludeFullPath"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath metodu. C++'da tam dosya yolu adının dahil edilip edilmeyeceğini alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


Tam dosya yolu adını içerip içermeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


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

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
