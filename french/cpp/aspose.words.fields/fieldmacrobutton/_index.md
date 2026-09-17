---
title: "Classe Aspose::Words::Fields::FieldMacroButton"
linktitle: "FieldMacroButton"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Fields::FieldMacroButton. Implémente le champ MACROBUTTON. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 65000
url: /fr/cpp/aspose.words.fields/fieldmacrobutton/
---
## FieldMacroButton class


Implémente le champ MACROBUTTON. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMacroButton : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_DisplayText](./get_displaytext/)() | Obtient ou définit le texte à afficher comme le "bouton" sélectionné pour exécuter la macro ou la commande. |
| [get_End](./get_end/)() override | Obtient le nœud qui représente la fin du champ. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_MacroName](./get_macroname/)() | Obtient ou définit le nom de la macro ou de la commande à exécuter. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](./get_separator/)() override | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](./get_start/)() override | Obtient le nœud qui représente le début du champ. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_DisplayText](./set_displaytext/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldMacroButton::get_DisplayText](./get_displaytext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_MacroName](./set_macroname/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldMacroButton::get_MacroName](./get_macroname/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Remarques


Permet d'exécuter une macro ou une commande.

Dans Aspose.Words, ce champ peut également servir de champ de fusion.

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
