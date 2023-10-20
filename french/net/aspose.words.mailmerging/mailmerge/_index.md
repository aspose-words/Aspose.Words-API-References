---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words pour .NET
description: Aspose.Words.MailMerging.MailMerge classe. Représente la fonctionnalité de publipostage en C#.
type: docs
weight: 3840
url: /fr/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Représente la fonctionnalité de publipostage.

Pour en savoir plus, visitez le[Fusion et publipostage et création de rapports](https://docs.aspose.com/words/net/mail-merge-and-reporting/) article documentaire.

```csharp
public class MailMerge
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Obtient ou définit un ensemble d'indicateurs qui spécifient les éléments qui doivent être supprimés lors du publipostage. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Obtient ou définit une valeur indiquant si les paragraphes avec des signes de ponctuation sont considérés comme vides et doivent être supprimés si leRemoveEmptyParagraphs l'option est spécifiée. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Se produit lors du publipostage lorsqu'un champ de publipostage est rencontré dans le document. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Permet de gérer des événements particuliers lors du publipostage. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Renvoie une collection qui représente les champs de données mappés pour l'opération de publipostage. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Obtient ou définit une valeur indiquant si toutes les régions de publipostage de documents portant le nom d'une source de données doivent être fusionnées lors de l'exécution d'un publipostage avec des régions par rapport à la source de données ou uniquement la première. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Obtient ou définit une valeur indiquant si les champs de l'ensemble du document sont mis à jour lors de l'exécution d'un publipostage avec des régions. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Obtient ou définit une valeur indiquant si les balises "moustache" inutilisées doivent être conservées. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Obtient ou définit une balise de fin de région de fusion et publipostage. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Obtient ou définit une balise de début de région de fusion et publipostage. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Obtient ou définit une valeur indiquant si les listes sont redémarrées à chaque section après l'exécution d'un publipostage. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Obtient ou définit une valeur indiquant si le[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) de la première section du document et ses copies pour les lignes de source de données suivantes sont conservées lors du publipostage ou mises à jour selon le comportement de MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Obtient ou définit une valeur indiquant si les espaces de fin et de début sont supprimés des valeurs de publipostage. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Obtient ou définit une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés quelle que soit la condition du champ IF parent. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Quand`vrai` , spécifie qu'en plus des champs MERGEFIELD, le publipostage est effectué dans d'autres types de champs et également dans les balises "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Obtient ou définit une valeur indiquant si un paragraphe entier avec**Début de la table** ou**Fin de table** field ou plage particulière entre**Début de la table** et**Fin de table** les champs doivent être inclus dans la région de publipostage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Supprime les champs liés au publipostage du document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Effectue un publipostage à partir d'un**Ligne de données** dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Effectue le publipostage d'un DataTable dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Effectue un publipostage à partir d'un**Vue de données** dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Effectue un publipostage à partir de**IDataReader** dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Effectue un publipostage à partir d'une source de données personnalisée. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Effectue une opération de publipostage pour un seul enregistrement. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | Effectue un publipostage à partir d'un objet ADO Recordset dans le document. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Effectue un publipostage à partir d'un**Base de données** dans un document avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Effectue un publipostage à partir d'un**Table de données** dans le document avec les régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Effectue un publipostage à partir d'un**Vue de données** dans le document avec les régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Effectue un publipostage à partir d'une source de données personnalisée avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Effectue un publipostage à partir d'une source de données personnalisée avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Effectue un publipostage à partir de**IDataReader** dans le document avec les régions de publipostage. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | Effectue un publipostage à partir d'un objet ADO Recordset dans le document avec des régions de publipostage. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Renvoie une collection de noms de champs de publipostage disponibles dans le document. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Renvoie une collection de noms de champs de publipostage disponibles dans la région. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Renvoie une collection de noms de champs de publipostage disponibles dans la région. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Renvoie une collection de régions de publipostage portant le nom spécifié. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Renvoie une hiérarchie complète des régions (avec champs) disponibles dans le document. |

## Remarques

Pour que l'opération de publipostage fonctionne, le document doit contenir les champs Word MERGEFIELD et éventuellement NEXT. Lors de l'opération de publipostage, les champs de fusion du document sont remplacés par les valeurs de votre source de données.

Il existe deux manières distinctes d'utiliser le publipostage : avec et sans régions de publipostage.

Le publipostage le plus simple est sans régions et il est très similaire au fonctionnement de mail merge dans Word. UtiliserExécuter méthodes pour fusionner les informations de la source de données some telle que**Table de données** ,**Base de données** ,**Vue de données** ,**IDataReader** ou un tableau d'objets dans votre document. Le `MailMerge` L'objet traite tous les enregistrements de la source de données et copie et ajoute le contenu de l'ensemble du document pour chaque enregistrement.

Notez que lorsque`MailMerge` L'objet rencontre un champ NEXT, il sélectionne l'enregistrement suivant dans la source de données et continue la fusion sans copier aucun contenu.

Utiliser[`ExecuteWithRegions`](./executewithregions/) et d'autres surcharges pour fusionner des informations dans un document a avec des régions de fusion et de publipostage définies. Vous pouvez utiliser **Base de données** ,**Table de données** ,**Vue de données** ou**IDataReader** comme sources de données pour cette opération.

Vous devez utiliser des régions de fusion et publipostage si vous souhaitez agrandir dynamiquement des parties à l'intérieur du document . Sans régions de fusion et publipostage, le document entier sera répété pour chaque enregistrement de la source de données.

## Exemples

Montre comment exécuter un publipostage avec les données d'un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Vous trouverez ci-dessous deux manières d'utiliser un DataTable comme source de données pour un publipostage.
    // 1 - Utilisez le tableau entier pour le publipostage afin de créer un document de publipostage de sortie pour chaque ligne du tableau :
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilisez une ligne du tableau pour créer un document de publipostage en sortie :
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crée un document source de publipostage.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Voir également

* espace de noms [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../)
