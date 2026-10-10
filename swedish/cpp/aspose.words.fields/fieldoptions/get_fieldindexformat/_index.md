---
title: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat metod"
linktitle: "get_FieldIndexFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat metod. Hämtar eller anger ett FieldIndexFormat som representerar formateringen för FieldIndex-fälten i dokumentet i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.fields/fieldoptions/get_fieldindexformat/
---
## FieldOptions::get_FieldIndexFormat method


Hämtar eller anger ett [FieldIndexFormat](./) som representerar formateringen för [FieldIndex](../../fieldindex/) fälten i dokumentet.

```cpp
Aspose::Words::Fields::FieldIndexFormat Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat()
```


## Exempel



Visar hur man formaterar [FieldIndex](../../fieldindex/) fält.
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

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
