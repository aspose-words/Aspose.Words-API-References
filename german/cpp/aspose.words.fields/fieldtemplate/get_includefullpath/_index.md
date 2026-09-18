---
title: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath Methode"
linktitle: "get_IncludeFullPath"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath Methode. Liest oder setzt, ob der vollständige Dateipfadname in C++ einbezogen werden soll."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


Ruft ab oder legt fest, ob der vollständige Dateipfadname einbezogen werden soll.

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


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

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
