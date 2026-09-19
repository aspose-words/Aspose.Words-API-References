---
title: "Metodo Aspose::Words::Fields::FormField::get_Type"
linktitle: "get_Type"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FormField::get_Type. Restituisce il tipo di campo modulo in C++."
type: docs
weight: 24000
url: /it/cpp/aspose.words.fields/formfield/get_type/
---
## FormField::get_Type method


Restituisce il tipo di campo modulo.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FormField::get_Type()
```


## Esempi



Mostra come inserire una casella combinata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Inserisci una casella combinata che consentirà all'utente di scegliere un'opzione da una raccolta di stringhe.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Il campo modulo apparirà sotto forma di tag html "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## Vedi anche

* Enum [FieldType](../../fieldtype/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
