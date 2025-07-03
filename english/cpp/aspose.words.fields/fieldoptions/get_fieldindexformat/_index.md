---
title: Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat method
linktitle: get_FieldIndexFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat method. Gets or sets a FieldIndexFormat that represents the formatting for the FieldIndex fields in the document in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.fields/fieldoptions/get_fieldindexformat/
---
## FieldOptions::get_FieldIndexFormat method


Gets or sets a [FieldIndexFormat](./) that represents the formatting for the [FieldIndex](../../fieldindex/) fields in the document.

```cpp
Aspose::Words::Fields::FieldIndexFormat Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat()
```


## Examples



Shows how to formatting [FieldIndex](../../fieldindex/) fields. 
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

## See Also

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
