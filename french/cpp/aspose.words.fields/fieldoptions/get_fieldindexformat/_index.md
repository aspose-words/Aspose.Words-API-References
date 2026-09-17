---
title: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat méthode"
linktitle: "get_FieldIndexFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat méthode. Obtient ou définit un FieldIndexFormat qui représente le formatage des champs FieldIndex dans le document en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.fields/fieldoptions/get_fieldindexformat/
---
## FieldOptions::get_FieldIndexFormat method


Obtient ou définit un [FieldIndexFormat](./) qui représente le formatage des champs [FieldIndex](../../fieldindex/) dans le document.

```cpp
Aspose::Words::Fields::FieldIndexFormat Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat()
```


## Exemples



Montre comment formater les champs [FieldIndex](../../fieldindex/).
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

## Voir aussi

* Enum [FieldIndexFormat](../../fieldindexformat/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
