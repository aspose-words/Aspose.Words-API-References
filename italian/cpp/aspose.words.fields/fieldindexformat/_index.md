---
title: "Aspose::Words::Fields::FieldIndexFormat enum"
linktitle: "FieldIndexFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldIndexFormat enum. Specifica la formattazione per i campi FieldIndex in un documento in C++."
type: docs
weight: 129000
url: /it/cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


Specifica la formattazione per i campi [FieldIndex](../fieldindex/) in un documento.

```cpp
enum class FieldIndexFormat
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Modello | 0 | Dal modello. |
| Classico | 1 | Classico. |
| Elegante | 2 | Elegante. |
| Modern | 3 | Moderno. |
| Puntato | 4 | Puntato. |
| Formale | 5 | Formale. |
| Semplice | 6 | Semplice. |


## Esempi



Mostra come formattare i campi [FieldIndex](../fieldindex/).
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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
