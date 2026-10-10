---
title: "Aspose::Words::Replacing::FindReplaceOptions classe"
linktitle: "FindReplaceOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions classe. Spécifie les options pour les opérations de recherche/remplacement. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


Spécifie les options pour les opérations de recherche/remplacement. Pour en savoir plus, consultez l'article de documentation [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/).

```cpp
class FindReplaceOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | Initialise une nouvelle instance de la classe [FindReplaceOptions](./) avec les paramètres par défaut. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | Initialise une nouvelle instance de la classe [FindReplaceOptions](./) avec la direction spécifiée. |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Initialise une nouvelle instance de la classe [FindReplaceOptions](./) avec le rappel de remplacement spécifié. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Initialise une nouvelle instance de la classe [FindReplaceOptions](./) avec la direction et le rappel de remplacement spécifiés. |
| [get_ApplyFont](./get_applyfont/)() const | Mise en forme du texte appliquée au nouveau contenu. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | Mise en forme du [Paragraph](../../aspose.words/paragraph/) appliquée au nouveau contenu. |
| [get_Direction](./get_direction/)() const | Sélectionne la direction du remplacement. La valeur par défaut est [Forward](../findreplacedirection/). |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True indique que oldValue doit être un mot autonome. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions de suppression. La valeur par défaut est **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des codes de champ. La valeur par défaut est **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des champs. La valeur par défaut est **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les notes de bas de page. La valeur par défaut est **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions d'insertion. La valeur par défaut est **false**. |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur d'OfficeMath/>. La valeur par défaut est **true**. |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les formes à l'intérieur d'un texte. La valeur par défaut est **false**. |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le contenu de [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). La valeur par défaut est **false**. |
| [get_LegacyMode](./get_legacymode/)() const | Obtient ou définit une valeur booléenne indiquant que l'ancien algorithme de recherche/remplacement est utilisé. |
| [get_MatchCase](./get_matchcase/)() const | True indique une comparaison sensible à la casse, false indique une comparaison insensible à la casse. |
| [get_ReplacementFormat](./get_replacementformat/)() const | Spécifie le format du remplacement. La valeur par défaut est [Texte](../replacementformat/). |
| [get_ReplacingCallback](./get_replacingcallback/)() const | La méthode définie par l'utilisateur qui est appelée avant chaque occurrence de remplacement. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | Obtient ou définit une valeur booléenne indiquant s'il est autorisé de remplacer le saut de paragraphe lorsqu'il n'existe pas de paragraphe frère suivant. La valeur par défaut est **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | Vrai indique qu'une recherche de texte est effectuée séquentiellement de haut en bas en tenant compte des zones de texte. La valeur par défaut est **false**. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut reconnaître et utiliser les substitutions dans les modèles de remplacement. La valeur par défaut est **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | Sélectionne la direction du remplacement. La valeur par défaut est [Forward](../findreplacedirection/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/). |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/). |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/). |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath](./get_ignoreofficemath/). |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes](./get_ignoreshapes/). |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/). |
| [set_LegacyMode](./set_legacymode/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/). |
| [set_MatchCase](./set_matchcase/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/). |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | Spécifie le format du remplacement. La valeur par défaut est [Texte](../replacementformat/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | La méthode définie par l'utilisateur qui est appelée avant chaque occurrence de remplacement. |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/). |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | Vrai indique qu'une recherche de texte est effectuée séquentiellement de haut en bas en tenant compte des zones de texte. La valeur par défaut est **false**. |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | Définisseur pour [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment activer/désactiver la sensibilité à la casse lors d'une opération de recherche et remplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez le drapeau "MatchCase" sur "true" pour appliquer la sensibilité à la casse lors de la recherche des chaînes à remplacer.
// Définissez le drapeau "MatchCase" sur "false" pour ignorer la casse des caractères lors de la recherche du texte à remplacer.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Montre comment activer/désactiver les opérations de recherche et remplacement limitées aux mots isolés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez le drapeau "FindWholeWordsOnly" sur "true" pour remplacer le texte trouvé s'il ne fait pas partie d'un autre mot.
// Définissez le drapeau "FindWholeWordsOnly" sur "false" pour remplacer tout le texte, quel que soit son contexte.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Voir aussi

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
