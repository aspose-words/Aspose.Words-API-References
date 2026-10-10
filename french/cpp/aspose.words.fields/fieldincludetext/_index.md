---
title: "Classe Aspose::Words::Fields::FieldIncludeText"
linktitle: "FieldIncludeText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Fields::FieldIncludeText. Implémente le champ INCLUDETEXT. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 58000
url: /fr/cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


Implémente le champ INCLUDETEXT. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                         public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Obtient le nom du signet dans le document à inclure. |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_Encoding](./get_encoding/)() | Obtient l'encodage appliqué aux données du fichier référencé. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_LockFields](./get_lockfields/)() override | Obtient si les champs du document inclus doivent être empêchés d'être mis à jour. |
| [get_MimeType](./get_mimetype/)() | Obtient le type MIME du fichier référencé. |
| [get_NamespaceMappings](./get_namespacemappings/)() override | Obtient les mappages d'espaces de noms pour les requêtes XPath. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_SourceFullName](./get_sourcefullname/)() override | Obtient l'emplacement du document à l'aide d'un IRI. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| [get_TextConverter](./get_textconverter/)() override | Obtient le nom du convertisseur de texte pour le format du fichier inclus. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [get_XPath](./get_xpath/)() override | Obtient le XPath pour la partie souhaitée du fichier XML. |
| [get_XslTransformation](./get_xsltransformation/)() override | Obtient l'emplacement de la transformation XSL pour formater les données XML. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Définit le nom du signet dans le document à inclure. |
| [set_Encoding](./set_encoding/)(const System::String\&) | Définit l'encodage appliqué aux données du fichier référencé. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LockFields](./set_lockfields/)(bool) | Définit si les champs du document inclus doivent être empêchés d'être mis à jour. |
| [set_MimeType](./set_mimetype/)(const System::String\&) | Définit le type MIME du fichier référencé. |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | Définit les mappages d'espaces de noms pour les requêtes XPath. |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Définit l'emplacement du document à l'aide d'un IRI. |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Définit le nom du convertisseur de texte pour le format du fichier inclus. |
| [set_XPath](./set_xpath/)(const System::String\&) | Définit le XPath pour la partie souhaitée du fichier XML. |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | Définit l'emplacement de la transformation XSL pour formater les données XML. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |
## Voir aussi

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
