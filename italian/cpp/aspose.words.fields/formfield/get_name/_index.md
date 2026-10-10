---
title: "Aspose::Words::Fields::FormField::get_Name metodo"
linktitle: "get_Name"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FormField::get_Name metodo. Ottiene o imposta il nome del campo modulo in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.fields/formfield/get_name/
---
## FormField::get_Name method


Ottiene o imposta il nome del campo modulo.

```cpp
System::String Aspose::Words::Fields::FormField::get_Name()
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

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
