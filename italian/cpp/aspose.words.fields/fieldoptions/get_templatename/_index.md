---
title: "Metodo Aspose::Words::Fields::FieldOptions::get_TemplateName"
linktitle: "get_TemplateName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldOptions::get_TemplateName. Ottiene o imposta il nome file del modello utilizzato dal documento in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.fields/fieldoptions/get_templatename/
---
## FieldOptions::get_TemplateName method


Ottiene o imposta il nome file del modello utilizzato dal documento.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_TemplateName() const
```

## Note


Questa proprietà è utilizzata dal campo [FieldTemplate](../../fieldtemplate/) se la proprietà [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/) è vuota.

Se questa proprietà è vuota, viene utilizzato il nome file del modello predefinito **Normal.dotm**.

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

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
