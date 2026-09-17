---
title: "Aspose::Words::LowCode::MailMergeOptions class"
linktitle: "MailMergeOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::MailMergeOptions class. Représente les options pour la fonctionnalité de fusion de courrier en C++."
type: docs
weight: 750
url: /fr/cpp/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class


Représente les options pour la fonctionnalité de publipostage.

```cpp
class MailMergeOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Obtient un ensemble de drapeaux qui spécifient quels éléments doivent être supprimés lors de la fusion de courrier. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Obtient ou définit une valeur indiquant si les paragraphes contenant des signes de ponctuation sont considérés comme vides et doivent être supprimés si l'option [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/) est spécifiée. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Obtient une valeur indiquant si toutes les régions de fusion de courrier du document portant le nom d'une source de données doivent être fusionnées lors de l'exécution d'une fusion de courrier avec régions contre la source de données ou seulement la première. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Obtient une valeur indiquant si les champs de l'ensemble du document sont mis à jour lors de l'exécution d'une fusion de courrier avec régions. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Obtient une valeur indiquant si les balises "mustache" inutilisées doivent être conservées. |
| [get_RegionEndTag](./get_regionendtag/)() const | Obtient la balise de fin de région de fusion de courrier. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Obtient la balise de début de région de fusion de courrier. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Obtient une valeur indiquant si les listes sont redémarrées à chaque section après l'exécution d'une fusion de courrier. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Obtient une valeur indiquant si le début de section de la première section du document et ses copies pour les lignes de source de données suivantes sont conservés pendant la fusion de courrier ou mis à jour selon le comportement de MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Obtient une valeur indiquant si les espaces blancs en début et en fin sont supprimés des valeurs de fusion de courrier. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Obtient une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés indépendamment de la condition du champ IF parent. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Lorsque **true**, spécifie qu'en plus des champs MERGEFIELD, la fusion de courrier est effectuée dans d'autres types de champs et également dans les balises "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Obtient une valeur indiquant si le paragraphe complet contenant le champ **TableStart** ou **TableEnd**, ou la plage particulière entre les champs **TableStart** et **TableEnd**, doit être inclus dans la région de fusion de courrier. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Définit un ensemble de drapeaux qui spécifient quels éléments doivent être supprimés lors de la fusion de courrier. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Mutateur pour [Aspose::Words::LowCode::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Définit une valeur indiquant si toutes les régions de fusion de courrier du document portant le nom d’une source de données doivent être fusionnées lors de l’exécution d’une fusion de courrier avec régions sur la source de données ou uniquement la première. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Définit une valeur indiquant si les champs dans l’ensemble du document sont mis à jour lors de l’exécution d’une fusion de courrier avec régions. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Définit une valeur indiquant si les balises "mustache" inutilisées doivent être conservées. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Définit une balise de fin de région de fusion de courrier. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Définit une balise de début de région de fusion de courrier. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Définit une valeur indiquant si les listes sont redémarrées à chaque section après l’exécution d’une fusion de courrier. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Définit une valeur indiquant si le début de section de la première section du document et ses copies pour les lignes suivantes de la source de données sont conservés pendant la fusion de courrier ou mis à jour selon le comportement de MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Définit une valeur indiquant si les espaces blancs en début et en fin sont supprimés des valeurs de fusion de courrier. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Définit une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés indépendamment de la condition du champ IF parent. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Mutateur pour [Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Définit une valeur indiquant si le paragraphe complet contenant le champ **TableStart** ou **TableEnd**, ou la plage particulière entre les champs **TableStart** et **TableEnd**, doit être inclus dans la région de fusion de courrier. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
