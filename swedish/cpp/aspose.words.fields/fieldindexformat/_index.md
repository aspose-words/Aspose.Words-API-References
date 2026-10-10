---
title: "Aspose::Words::Fields::FieldIndexFormat enum"
linktitle: "FieldIndexFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIndexFormat-enum. Anger formateringen för FieldIndex-fält i ett dokument i C++."
type: docs
weight: 129000
url: /sv/cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


Anger formateringen för [FieldIndex](../fieldindex/)-fält i ett dokument.

```cpp
enum class FieldIndexFormat
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Mall | 0 | Från mall. |
| Klassisk | 1 | Klassisk. |
| Fantasifull | 2 | Fantasifull. |
| Modern | 3 | Modern. |
| Punktlista | 4 | Punktlista. |
| Formell | 5 | Formell. |
| Enkel | 6 | Enkel. |


## Exempel



Visar hur man formaterar [FieldIndex](../fieldindex/) fält.
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

## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
