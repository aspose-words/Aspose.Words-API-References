---
title: "Aspose::Words::Fields::FieldOptions::get_TemplateName method"
linktitle: "get_TemplateName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions::get_TemplateName method. Liest oder setzt den Dateinamen der vom Dokument in C++ verwendeten Vorlage."
type: docs
weight: 19000
url: /de/cpp/aspose.words.fields/fieldoptions/get_templatename/
---
## FieldOptions::get_TemplateName method


Liest oder legt den Dateinamen der vom Dokument verwendeten Vorlage fest.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_TemplateName() const
```

## Hinweise


Diese Eigenschaft wird vom [FieldTemplate](../../fieldtemplate/)-Feld verwendet, wenn die [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/)-Eigenschaft leer ist.

Ist diese Eigenschaft leer, wird der Standardvorlagen-Dateiname **Normal.dotm** verwendet.

## Beispiele



Zeigt, wie man ein TEMPLATE-Feld verwendet, um den Speicherort der Dokumentvorlage im lokalen Dateisystem anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wir können einen Vorlagennamen über die Felder festlegen. Diese Eigenschaft wird verwendet, wenn \"doc.AttachedTemplate\" leer ist.
// Wenn diese Eigenschaft leer ist, wird der Standardvorlagendateiname \"Normal.dotm\" verwendet.
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

## Siehe auch

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
