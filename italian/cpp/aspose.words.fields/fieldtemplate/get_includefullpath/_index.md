---
title: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath metodo"
linktitle: "get_IncludeFullPath"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath metodo. Ottiene o imposta se includere il nome completo del percorso file in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


Ottiene o imposta se includere il nome completo del percorso del file.

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


## Esempi



Mostra come utilizzare un campo TEMPLATE per visualizzare la posizione nel file system locale del modello di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Possiamo impostare un nome di modello utilizzando i campi. Questa proprietà è usata quando \"doc.AttachedTemplate\" è vuoto.
// Se questa proprietà è vuota, viene utilizzato il nome file del modello predefinito \"Normal.dotm\".
doc->get_FieldOptions()->set_TemplateName(System::String::Empty);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
ASSERT_EQ(u" TEMPLATE ", field->GetFieldCode());

builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
field->set_IncludeFullPath(true);

ASSERT_EQ(u" TEMPLATE  \\p", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TEMPLATE.docx");
```

## Vedi anche

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
