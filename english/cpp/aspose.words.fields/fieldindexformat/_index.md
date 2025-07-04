---
title: Aspose::Words::Fields::FieldIndexFormat enum
linktitle: FieldIndexFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldIndexFormat enum. Specifies the formatting for the FieldIndex fields in a document in C++.'
type: docs
weight: 129000
url: /cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


Specifies the formatting for the [FieldIndex](../fieldindex/) fields in a document.

```cpp
enum class FieldIndexFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Template | 0 | From template. |
| Classic | 1 | Classic. |
| Fancy | 2 | Fancy. |
| Modern | 3 | Modern. |
| Bulleted | 4 | Bulleted. |
| Formal | 5 | Formal. |
| Simple | 6 | Simple. |


## Examples



Shows how to formatting [FieldIndex](../fieldindex/) fields. 
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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
