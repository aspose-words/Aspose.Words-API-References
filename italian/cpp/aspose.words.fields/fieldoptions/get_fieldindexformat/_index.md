---
title: "Metodo Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat"
linktitle: "get_FieldIndexFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat. Ottiene o imposta un FieldIndexFormat che rappresenta la formattazione per i campi FieldIndex nel documento in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.fields/fieldoptions/get_fieldindexformat/
---
## FieldOptions::get_FieldIndexFormat method


Ottiene o imposta un [FieldIndexFormat](./) che rappresenta la formattazione per i campi [FieldIndex](../../fieldindex/) nel documento.

```cpp
Aspose::Words::Fields::FieldIndexFormat Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat()
```


## Esempi



Mostra come formattare i campi [FieldIndex](../../fieldindex/).
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

## Vedi anche

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
