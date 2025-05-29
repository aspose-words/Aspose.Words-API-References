---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.MailMergeOptions pour des solutions de publipostage low-code fluides. Optimisez l'automatisation de vos documents grâce à des fonctionnalités personnalisables !
type: docs
weight: 4260
url: /fr/net/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class

Représente les options pour la fonctionnalité de publipostage.

```csharp
public class MailMergeOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode/mailmergeoptions/cleanupoptions/) { get; set; } | Obtient ou définit un ensemble d'indicateurs qui spécifient les éléments à supprimer lors du publipostage. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | Obtient ou définit une valeur indiquant si les paragraphes avec des signes de ponctuation sont considérés comme vides et doivent être supprimés si leRemoveEmptyParagraphs l'option est spécifiée. |
| [MergeDuplicateRegions](../../aspose.words.lowcode/mailmergeoptions/mergeduplicateregions/) { get; set; } | Obtient ou définit une valeur indiquant si toutes les régions de publipostage de document portant le nom d'une source de données doivent être fusionnées lors de l'exécution d'un publipostage avec des régions par rapport à la source de données ou uniquement la première. |
| [MergeWholeDocument](../../aspose.words.lowcode/mailmergeoptions/mergewholedocument/) { get; set; } | Obtient ou définit une valeur indiquant si les champs de l'ensemble du document sont mis à jour lors de l'exécution d'un publipostage avec des régions. |
| [PreserveUnusedTags](../../aspose.words.lowcode/mailmergeoptions/preserveunusedtags/) { get; set; } | Obtient ou définit une valeur indiquant si les balises « moustache » inutilisées doivent être conservées. |
| [RegionEndTag](../../aspose.words.lowcode/mailmergeoptions/regionendtag/) { get; set; } | Obtient ou définit une balise de fin de région de publipostage. |
| [RegionStartTag](../../aspose.words.lowcode/mailmergeoptions/regionstarttag/) { get; set; } | Obtient ou définit une balise de début de région de publipostage. |
| [RestartListsAtEachSection](../../aspose.words.lowcode/mailmergeoptions/restartlistsateachsection/) { get; set; } | Obtient ou définit une valeur indiquant si les listes sont redémarrées à chaque section après l'exécution d'un publipostage. |
| [RetainFirstSectionStart](../../aspose.words.lowcode/mailmergeoptions/retainfirstsectionstart/) { get; set; } | Obtient ou définit une valeur indiquant si le début de la section de la première section du document et ses copies pour les lignes de source de données suivantes sont conservés pendant le publipostage ou mis à jour conformément au comportement de MS Word. |
| [TrimWhitespaces](../../aspose.words.lowcode/mailmergeoptions/trimwhitespaces/) { get; set; } | Obtient ou définit une valeur indiquant si les espaces de fin et de début sont supprimés des valeurs de publipostage. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | Obtient ou définit une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés quelle que soit la condition du champ IF parent. |
| [UseNonMergeFields](../../aspose.words.lowcode/mailmergeoptions/usenonmergefields/) { get; set; } | Quand`vrai` , spécifie qu'en plus des champs MERGEFIELD, le publipostage est effectué dans certains autres types de champs et également dans les balises "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | Obtient ou définit une valeur indiquant si le paragraphe entier avec**TableStart** ou**Fin de table** field ou plage particulière entre**TableStart** et**Fin de table** les champs doivent être inclus dans la région de publipostage. |

## Exemples

Montre comment effectuer une opération de publipostage pour un seul enregistrement.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage :
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Voir également

* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
