---
title: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat método"
linktitle: "get_FieldIndexFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat método. Obtiene o establece un FieldIndexFormat que representa el formato de los campos FieldIndex en el documento en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.fields/fieldoptions/get_fieldindexformat/
---
## FieldOptions::get_FieldIndexFormat method


Obtiene o establece un [FieldIndexFormat](./) que representa el formato de los campos [FieldIndex](../../fieldindex/) en el documento.

```cpp
Aspose::Words::Fields::FieldIndexFormat Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat()
```


## Ejemplos



Muestra cómo formatear los campos [FieldIndex](../../fieldindex/).
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

## Ver también

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
