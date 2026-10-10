---
title: "Aspose::Words::Fields::FieldIndexFormat enum"
linktitle: "FieldIndexFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldIndexFormat enum. Spécifie le formatage des champs FieldIndex dans un document en C++."
type: docs
weight: 129000
url: /fr/cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


Spécifie le formatage des champs [FieldIndex](../fieldindex/) dans un document.

```cpp
enum class FieldIndexFormat
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Modèle | 0 | À partir du modèle. |
| Classique | 1 | Classique. |
| Fantaisie | 2 | Fantaisie. |
| Modern | 3 | Moderne. |
| À puces | 4 | À puces. |
| Formel | 5 | Formel. |
| Simple | 6 | Simple. |


## Exemples



Montre comment formater les champs [FieldIndex](../fieldindex/).
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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
