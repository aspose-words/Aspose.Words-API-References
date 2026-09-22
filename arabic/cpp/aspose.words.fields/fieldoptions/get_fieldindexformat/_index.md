---
title: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat طريقة"
linktitle: "get_FieldIndexFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat method. يحصل أو يضبط FieldIndexFormat الذي يمثل تنسيق حقول FieldIndex في المستند في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.fields/fieldoptions/get_fieldindexformat/
---
## FieldOptions::get_FieldIndexFormat method


يحصل أو يضبط [FieldIndexFormat](./) الذي يمثل تنسيق حقول [FieldIndex](../../fieldindex/) في المستند.

```cpp
Aspose::Words::Fields::FieldIndexFormat Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat()
```


## أمثلة



يعرض كيفية تنسيق حقول [FieldIndex](../../fieldindex/).
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

## انظر أيضًا

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
