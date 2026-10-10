---
title: "Aspose::Words::Fields::FieldMacroButton::get_MacroName méthode"
linktitle: "get_MacroName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldMacroButton::get_MacroName method. Obtient ou définit le nom de la macro ou de la commande à exécuter en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fields/fieldmacrobutton/get_macroname/
---
## FieldMacroButton::get_MacroName method


Obtient ou définit le nom de la macro ou de la commande à exécuter.

```cpp
System::String Aspose::Words::Fields::FieldMacroButton::get_MacroName()
```


## Exemples



Montre comment utiliser les champs MACROBUTTON pour nous permettre d'exécuter les macros d'un document en cliquant.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// Insérez un champ MACROBUTTON et référencez l'une des macros du document par son nom dans la propriété MacroName.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// Utilisez la propriété pour référencer "ViewZoom200", une macro fournie avec Microsoft Word.
// Nous pouvons trouver toutes les autres macros via Affichage -> Macros (menu déroulant) -> Afficher les macros.
// Dans ce menu, sélectionnez "Word Commands" dans la liste déroulante "Macros in:".
// Si notre document contient une macro personnalisée portant le même nom qu'une macro standard,
// notre macro sera celle que le champ MACROBUTTON exécute.
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// Enregistrez le document en tant que type de document activé pour les macros.
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## Voir aussi

* Class [FieldMacroButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
