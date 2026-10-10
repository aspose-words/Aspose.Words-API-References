---
title: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat-Methode"
linktitle: "get_FieldIndexFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat-Methode. Ruft ein FieldIndexFormat ab oder legt es fest, das die Formatierung für die FieldIndex‑Felder im Dokument in C++ darstellt."
type: docs
weight: 9000
url: /de/cpp/aspose.words.fields/fieldoptions/get_fieldindexformat/
---
## FieldOptions::get_FieldIndexFormat method


Liest oder setzt ein [FieldIndexFormat](./), das die Formatierung für die [FieldIndex](../../fieldindex/)-Felder im Dokument darstellt.

```cpp
Aspose::Words::Fields::FieldIndexFormat Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat()
```


## Beispiele



Zeigt, wie man [FieldIndex](../../fieldindex/)-Felder formatiert.
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

## Siehe auch

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
