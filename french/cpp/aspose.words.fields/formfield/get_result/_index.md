---
title: "Méthode Aspose::Words::Fields::FormField::get_Result"
linktitle: "get_Result"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FormField::get_Result. Obtient ou définit une chaîne qui représente le résultat de ce champ de formulaire en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


Obtient ou définit une chaîne qui représente le résultat de ce champ de formulaire.

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## Remarques


Pour un champ de formulaire texte, le résultat est le texte présent dans le champ.

Pour un champ de formulaire case à cocher, le résultat peut être "1" ou "0" pour indiquer coché ou décoché.

Pour un champ de formulaire déroulant, le résultat est la chaîne sélectionnée dans la liste déroulante.

Définir [Result](./) pour un champ de formulaire texte n'applique pas le format de texte spécifié dans [TextInputFormat](../get_textinputformat/). Si vous souhaitez définir une valeur et appliquer le format, utilisez la méthode [SetTextInputValue()](../).

Pour un champ de formulaire texte, la valeur [TextInputDefault](../get_textinputdefault/) est appliquée si *value* est **null**.

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

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
