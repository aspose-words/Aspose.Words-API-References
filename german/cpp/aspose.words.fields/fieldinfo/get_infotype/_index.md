---
title: "Aspose::Words::Fields::FieldInfo::get_InfoType Methode"
linktitle: "get_InfoType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldInfo::get_InfoType Methode. Ermittelt oder legt den Typ der einzufügenden Dokumenteigenschaft in C++ fest."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldinfo/get_infotype/
---
## FieldInfo::get_InfoType method


Liest oder setzt den Typ der einzufügenden Dokumenteigenschaft.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_InfoType()
```


## Beispiele



Zeigt, wie man mit INFO-Feldern arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Setzen Sie einen Wert für die integrierte Eigenschaft "Comments" und fügen Sie dann ein INFO-Feld ein, um den Wert dieser Eigenschaft anzuzeigen.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// Setzen eines Wertes für die NewValue-Eigenschaft des Feldes und Aktualisieren
// Das Feld überschreibt außerdem die entsprechende integrierte Eigenschaft mit dem neuen Wert.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## Siehe auch

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
