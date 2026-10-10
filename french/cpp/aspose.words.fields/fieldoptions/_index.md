---
title: "Aspose::Words::Fields::FieldOptions classe"
linktitle: "FieldOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldOptions classe. Représente les options permettant de contrôler le traitement des champs dans un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 77000
url: /fr/cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


Représente les options permettant de contrôler la gestion des champs dans un document. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | Obtient ou définit le générateur de code-barres personnalisé. |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | Obtient un fournisseur qui renvoie un style de bibliographie pour les champs [FieldBibliography](../fieldbibliography/) et [FieldCitation](../fieldcitation/). |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | Obtient ou définit les chemins des modèles intégrés de MS Word. |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | Obtient l’évaluateur d’expressions de comparaison de champ. |
| [get_CurrentUser](./get_currentuser/)() const | Obtient ou définit les informations de l’utilisateur actuel. |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | Obtient le séparateur de style personnalisé pour le commutateur \t dans le champ [FieldToc](../fieldtoc/). |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | Obtient ou définit le nom d’auteur par défaut du document. Si le nom de l’auteur est déjà spécifié dans les propriétés intégrées du document, cette option n’est pas prise en compte. |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | Obtient un fournisseur qui renvoie le résultat d’une requête pour le champ [FieldDatabase](../fielddatabase/). |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | Obtient ou définit un [FieldIndexFormat](./get_fieldindexformat/) qui représente le formatage des champs [FieldIndex](../fieldindex/) dans le document. |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | Obtient ou définit un fournisseur qui renvoie un objet de culture spécifique à chaque champ particulier. |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | Spécifie la culture à utiliser pour formater le résultat du champ. |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | Obtient l’implémentation de [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | Obtient l’implémentation de [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [get_FileName](./get_filename/)() const | Obtient ou définit le nom de fichier du document. |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | Obtient ou définit la valeur indiquant si le texte bidirectionnel est entièrement pris en charge lors de la mise à jour du champ ou non. |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | Obtient ou définit la valeur indiquant si le format numérique hérité (antérieur à AW 13.10) pour les champs est activé ou non. |
| [get_PreProcessCulture](./get_preprocessculture/)() const | Obtient ou définit la culture à utiliser pour prétraiter les valeurs de champ. |
| [get_ResultFormatter](./get_resultformatter/)() const | Permet de contrôler la façon dont le résultat du champ est formaté. |
| [get_TemplateName](./get_templatename/)() const | Obtient ou définit le nom de fichier du modèle utilisé par le document. |
| [get_ToaCategories](./get_toacategories/)() const | Obtient ou définit le tableau des catégories d’autorités. |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | Obtient ou définit la valeur indiquant si le format numérique est analysé en utilisant la culture invariante ou non. |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | Obtient ou définit le répondant aux invites de l’utilisateur lors de la mise à jour du champ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\>\&) | Obtient ou définit le générateur de code-barres personnalisé. |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\>\&) | Définit un fournisseur qui renvoie un style de bibliographie pour les champs [FieldBibliography](../fieldbibliography/) et [FieldCitation](../fieldcitation/). |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\>\&) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths](./get_builtintemplatespaths/). |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\>\&) | Définit l’évaluateur d’expressions de comparaison de champ. |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\>\&) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_CurrentUser](./get_currentuser/). |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String\&) | Définit le séparateur de style personnalisé pour le commutateur \t dans le champ [FieldToc](../fieldtoc/). |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor](./get_defaultdocumentauthor/). |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\>\&) | Définit un fournisseur qui renvoie un résultat de requête pour le champ [FieldDatabase](../fielddatabase/). |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat](./get_fieldindexformat/). |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\>\&) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/). |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureSource](./get_fieldupdateculturesource/). |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\>\&) | Définit l'implémentation de [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\>\&) | Définit l'implémentation de [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [set_FileName](./set_filename/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_FileName](./get_filename/). |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/). |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat](./get_legacynumberformat/). |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\>\&) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_PreProcessCulture](./get_preprocessculture/). |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\>\&) | Permet de contrôler la façon dont le résultat du champ est formaté. |
| [set_TemplateName](./set_templatename/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_TemplateName](./get_templatename/). |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\>\&) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_ToaCategories](./get_toacategories/). |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/). |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\>\&) | Définisseur pour [Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent](./get_userpromptrespondent/). |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
