---
title: get_FieldIndexFormat
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a FieldIndexFormat that represents the formatting for the FieldIndex fields in the document.
type: docs
weight: 105
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(ArtifactsDir + u"Field.SetFieldIndexFormat.docx");
```

## See Also

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
