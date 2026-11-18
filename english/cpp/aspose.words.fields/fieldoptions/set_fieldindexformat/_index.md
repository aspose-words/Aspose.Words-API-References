---
title: Aspose::Words::Fields::FieldOptions::set_FieldIndexFormat method
linktitle: set_FieldIndexFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::set_FieldIndexFormat method. Sets a FieldIndexFormat that represents the formatting for the FieldIndex fields in the document in C++.'
type: docs
weight: 32000
url: /cpp/aspose.words.fields/fieldoptions/set_fieldindexformat/
---
## FieldOptions::set_FieldIndexFormat method


Sets a [FieldIndexFormat](../get_fieldindexformat/) that represents the formatting for the [FieldIndex](../../fieldindex/) fields in the document.

```cpp
void Aspose::Words::Fields::FieldOptions::set_FieldIndexFormat(Aspose::Words::Fields::FieldIndexFormat value)
```

## Examples


Shows how to formatting FieldIndex fields.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(get_ArtifactsDir() + u"Field.SetFieldIndexFormat.docx");
```
## See Also

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
