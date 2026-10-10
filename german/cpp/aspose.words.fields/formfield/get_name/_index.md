---
title: "Aspose::Words::Fields::FormField::get_Name Methode"
linktitle: "get_Name"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FormField::get_Name Methode. Gibt den Namen des Formularfelds zurück oder setzt ihn in C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words.fields/formfield/get_name/
---
## FormField::get_Name method


Liest oder setzt den Namen des Formularfelds.

```cpp
System::String Aspose::Words::Fields::FormField::get_Name()
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

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
