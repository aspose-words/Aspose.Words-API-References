---
title: "Aspose::Words::Fields::FormField::get_Name metod"
linktitle: "get_Name"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FormField::get_Name metod. Hämtar eller anger formulärfältets namn i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.fields/formfield/get_name/
---
## FormField::get_Name method


Hämtar eller anger formulärfältets namn.

```cpp
System::String Aspose::Words::Fields::FormField::get_Name()
```


## Exempel



Visar hur man infogar en kombinationsruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Infoga en kombinationsruta som låter en användare välja ett alternativ från en samling strängar.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Formulärfältet kommer att visas i form av en "select"-HTML-tagg.
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## Se även

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
