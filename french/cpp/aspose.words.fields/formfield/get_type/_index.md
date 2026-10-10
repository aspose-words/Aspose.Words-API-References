---
title: "Aspose::Words::Fields::FormField::get_Type method"
linktitle: "get_Type"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FormField::get_Type method. Retourne le type du champ de formulaire en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words.fields/formfield/get_type/
---
## FormField::get_Type method


Renvoie le type de champ de formulaire.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FormField::get_Type()
```


## Exemples



Montre comment insérer une combo box.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Insérez une combo box qui permettra à l'utilisateur de choisir une option parmi une collection de chaînes.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Le champ de formulaire apparaîtra sous la forme d'une balise HTML "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## Voir aussi

* Enum [FieldType](../../fieldtype/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
