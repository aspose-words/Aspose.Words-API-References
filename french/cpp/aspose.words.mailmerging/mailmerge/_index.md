---
title: "Classe Aspose::Words::MailMerging::MailMerge"
linktitle: "MailMerge"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::MailMerging::MailMerge. Représente la fonctionnalité de publipostage. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.mailmerging/mailmerge/
---
## MailMerge class


Représente la fonctionnalité de fusion de courrier. Pour en savoir plus, consultez l'article de documentation [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMerge : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [DeleteFields](./deletefields/)() | Supprime les champs liés au publipostage du document. |
| [Execute](./execute/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Effectue un publipostage à partir d'une source de données personnalisée. |
| [Execute](./execute/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Effectue une opération de publipostage pour un enregistrement unique. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Effectue une fusion de courrier à partir d’une source de données personnalisée avec des régions de fusion de courrier. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) | Effectue une fusion de courrier à partir d’une source de données personnalisée avec des régions de fusion de courrier. |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Obtient un ensemble de drapeaux qui spécifient quels éléments doivent être supprimés lors de la fusion de courrier. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Obtient ou définit une valeur indiquant si les paragraphes contenant des signes de ponctuation sont considérés comme vides et doivent être supprimés si l’option [RemoveEmptyParagraphs](../mailmergecleanupoptions/) est spécifiée. |
| [get_FieldMergingCallback](./get_fieldmergingcallback/)() const | Se produit pendant la fusion de courrier lorsqu’un champ de fusion de courrier est rencontré dans le document. |
| [get_MailMergeCallback](./get_mailmergecallback/)() const | Permet de gérer des événements particuliers pendant la fusion de courrier. |
| [get_MappedDataFields](./get_mappeddatafields/)() | Renvoie une collection qui représente les champs de données mappés pour l’opération de fusion de courrier. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Obtient une valeur indiquant si toutes les régions de fusion de courrier du document portant le nom d'une source de données doivent être fusionnées lors de l'exécution d'une fusion de courrier avec régions contre la source de données ou seulement la première. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Obtient une valeur indiquant si les champs de l'ensemble du document sont mis à jour lors de l'exécution d'une fusion de courrier avec régions. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Obtient une valeur indiquant si les balises "mustache" inutilisées doivent être conservées. |
| [get_RegionEndTag](./get_regionendtag/)() const | Obtient la balise de fin de région de fusion de courrier. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Obtient la balise de début de région de fusion de courrier. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Obtient une valeur indiquant si les listes sont redémarrées à chaque section après l'exécution d'une fusion de courrier. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Obtient une valeur indiquant si le [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) de la première section du document et ses copies pour les lignes de source de données suivantes sont conservés pendant la fusion de courrier ou mis à jour selon le comportement de MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Obtient une valeur indiquant si les espaces blancs en début et en fin sont supprimés des valeurs de fusion de courrier. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Obtient une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés indépendamment de la condition du champ IF parent. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Lorsque **true**, spécifie qu'en plus des champs MERGEFIELD, la fusion de courrier est effectuée dans d'autres types de champs et également dans les balises "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Obtient une valeur indiquant si le paragraphe complet contenant le champ **TableStart** ou **TableEnd**, ou la plage particulière entre les champs **TableStart** et **TableEnd**, doit être inclus dans la région de fusion de courrier. |
| [GetFieldNames](./getfieldnames/)() | Renvoie une collection de noms de champs de fusion de courrier disponibles dans le document. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&) | Renvoie une collection de noms de champs de fusion de courrier disponibles dans la région. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&, int32_t) | Renvoie une collection de noms de champs de fusion de courrier disponibles dans la région. |
| [GetRegionsByName](./getregionsbyname/)(const System::String\&) | Renvoie une collection de régions de fusion de courrier portant le nom spécifié. |
| [GetRegionsHierarchy](./getregionshierarchy/)() | Renvoie une hiérarchie complète des régions (avec champs) disponibles dans le document. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Définit un ensemble de drapeaux qui spécifient quels éléments doivent être supprimés lors de la fusion de courrier. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Mutateur pour [Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_FieldMergingCallback](./set_fieldmergingcallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IFieldMergingCallback\>\&) | Se produit pendant la fusion de courrier lorsqu’un champ de fusion de courrier est rencontré dans le document. |
| [set_MailMergeCallback](./set_mailmergecallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeCallback\>\&) | Permet de gérer des événements particuliers pendant la fusion de courrier. |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Définit une valeur indiquant si toutes les régions de fusion de courrier du document portant le nom d’une source de données doivent être fusionnées lors de l’exécution d’une fusion de courrier avec régions sur la source de données ou uniquement la première. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Définit une valeur indiquant si les champs dans l’ensemble du document sont mis à jour lors de l’exécution d’une fusion de courrier avec régions. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Définit une valeur indiquant si les balises "mustache" inutilisées doivent être conservées. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Définit une balise de fin de région de fusion de courrier. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Définit une balise de début de région de fusion de courrier. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Définit une valeur indiquant si les listes sont redémarrées à chaque section après l’exécution d’une fusion de courrier. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Définit une valeur indiquant si le [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) de la première section du document et ses copies pour les lignes de source de données suivantes sont conservés pendant la fusion de courrier ou mis à jour selon le comportement de MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Définit une valeur indiquant si les espaces blancs en début et en fin sont supprimés des valeurs de fusion de courrier. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Définit une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés indépendamment de la condition du champ IF parent. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Mutateur pour [Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Définit une valeur indiquant si le paragraphe complet contenant le champ **TableStart** ou **TableEnd**, ou la plage particulière entre les champs **TableStart** et **TableEnd**, doit être inclus dans la région de fusion de courrier. |
| static [Type](./type/)() |  |
## Remarques


Pour que l’opération de fusion de courrier fonctionne, le document doit contenir des champs Word MERGEFIELD et éventuellement NEXT. Pendant l’opération de fusion de courrier, les champs de fusion dans le document sont remplacés par les valeurs de votre source de données.

Il existe deux manières distinctes d’utiliser la fusion de courrier : avec des régions de fusion de courrier et sans.

La fusion de courrier la plus simple se fait sans régions et est très similaire à la façon dont la fusion de courrier fonctionne dans Word. Utilisez les méthodes **Execute** pour fusionner des informations provenant d’une source de données telle que **DataTable**, **DataSet** ou un tableau d’objets dans votre document. L’objet [MailMerge](./) traite tous les enregistrements de la source de données et copie et ajoute le contenu du document complet pour chaque enregistrement.

Notez que lorsque l’objet [MailMerge](./) rencontre un champ NEXT, il sélectionne l’enregistrement suivant dans la source de données et continue la fusion sans copier aucun contenu.

Utilisez [ExecuteWithRegions()](../) et d’autres surcharges pour fusionner des informations dans un document avec des régions de fusion de courrier définies. Vous pouvez les utiliser comme sources de données pour cette opération.

Vous devez utiliser des régions de fusion de courrier si vous souhaitez faire croître dynamiquement des portions à l’intérieur du document. Sans régions de fusion de courrier, le document entier sera répété pour chaque enregistrement de la source de données.

## Voir aussi

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
