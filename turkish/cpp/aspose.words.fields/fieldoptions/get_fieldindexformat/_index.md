---
title: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat yöntemi."
linktitle: "get_FieldIndexFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat yöntemi. C++'ta belgede FieldIndex alanları için biçimlendirmeyi temsil eden bir FieldIndexFormat alır veya ayarlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.fields/fieldoptions/get_fieldindexformat/
---
## FieldOptions::get_FieldIndexFormat method


Belgedeki [FieldIndex](../../fieldindex/) alanları için biçimlendirmeyi temsil eden bir [FieldIndexFormat](./) alır veya ayarlar.

```cpp
Aspose::Words::Fields::FieldIndexFormat Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat()
```


## Örnekler



[FieldIndex](../../fieldindex/) alanlarını biçimlendirme nasıl yapılır gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(Aspose::Words::BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(Aspose::Words::Fields::FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(get_ArtifactsDir() + u"Field.SetFieldIndexFormat.docx");
```

## Ayrıca Bakınız

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
