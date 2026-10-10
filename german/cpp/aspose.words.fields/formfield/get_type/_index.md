---
title: "Aspose::Words::Fields::FormField::get_Type Methode"
linktitle: "get_Type"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FormField::get_Type Methode. Gibt den Typ des Formularfeldes in C++ zurück."
type: docs
weight: 24000
url: /de/cpp/aspose.words.fields/formfield/get_type/
---
## FormField::get_Type method


Gibt den Formularfeldtyp zurück.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FormField::get_Type()
```


## Beispiele



Zeigt, wie man ein Kombinationsfeld einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Fügt ein Kombinationsfeld ein, das es einem Benutzer ermöglicht, eine Option aus einer Sammlung von Zeichenketten auszuwählen.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Das Formularfeld wird in Form eines "select"-HTML-Tags angezeigt.
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## Siehe auch

* Enum [FieldType](../../fieldtype/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
