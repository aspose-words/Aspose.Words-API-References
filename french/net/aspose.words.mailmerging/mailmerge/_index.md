---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words pour .NET
description: Bénéficiez de puissantes fonctionnalités de publipostage avec la classe Aspose.Words.MailMerging.MailMerge. Simplifiez la création de documents et améliorez votre productivité sans effort !
type: docs
weight: 4530
url: /fr/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Représente la fonctionnalité de publipostage.

Pour en savoir plus, visitez le[Fusion et publipostage et création de rapports](https://docs.aspose.com/words/net/mail-merge-and-reporting/) article de documentation.

```csharp
public class MailMerge
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Obtient ou définit un ensemble d'indicateurs qui spécifient les éléments à supprimer lors du publipostage. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Obtient ou définit une valeur indiquant si les paragraphes avec des signes de ponctuation sont considérés comme vides et doivent être supprimés si leRemoveEmptyParagraphs l'option est spécifiée. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Se produit pendant le publipostage lorsqu'un champ de publipostage est rencontré dans le document. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Permet de gérer des événements particuliers lors du publipostage. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Renvoie une collection qui représente les champs de données mappés pour l'opération de publipostage. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Obtient ou définit une valeur indiquant si toutes les régions de publipostage de document portant le nom d'une source de données doivent être fusionnées lors de l'exécution d'un publipostage avec des régions par rapport à la source de données ou uniquement la première. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Obtient ou définit une valeur indiquant si les champs de l'ensemble du document sont mis à jour lors de l'exécution d'un publipostage avec des régions. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Obtient ou définit une valeur indiquant si les balises « moustache » inutilisées doivent être conservées. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Obtient ou définit une balise de fin de région de publipostage. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Obtient ou définit une balise de début de région de publipostage. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Obtient ou définit une valeur indiquant si les listes sont redémarrées à chaque section après l'exécution d'un publipostage. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Obtient ou définit une valeur indiquant si le[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) de la première section du document et de ses copies pour les lignes de source de données suivantes sont conservées lors du publipostage ou mises à jour conformément au comportement de MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Obtient ou définit une valeur indiquant si les espaces de fin et de début sont supprimés des valeurs de publipostage. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Obtient ou définit une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés quelle que soit la condition du champ IF parent. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Quand`vrai` , spécifie qu'en plus des champs MERGEFIELD, le publipostage est effectué dans certains autres types de champs et également dans les balises "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Obtient ou définit une valeur indiquant si le paragraphe entier avec**TableStart** ou**Fin de table** field ou plage particulière entre**TableStart** et**Fin de table** les champs doivent être inclus dans la région de publipostage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Supprime les champs liés au publipostage du document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Effectue le publipostage à partir d'un**Ligne de données** dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Effectue un publipostage à partir d'un DataTable vers le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Effectue le publipostage à partir d'un**Vue des données** dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Effectue le publipostage à partir de**IDataReader** dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Effectue un publipostage à partir d'une source de données personnalisée. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Effectue une opération de publipostage pour un seul enregistrement. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | Effectue un publipostage à partir d'un objet ADO Recordset dans le document. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Effectue le publipostage à partir d'un**Ensemble de données** dans un document avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Effectue le publipostage à partir d'un**Table de données** dans le document avec les régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Effectue le publipostage à partir d'un**Vue des données** dans le document avec les régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Effectue un publipostage à partir d'une source de données personnalisée avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Effectue un publipostage à partir d'une source de données personnalisée avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Effectue le publipostage à partir de**IDataReader** dans le document avec les régions de publipostage. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | Effectue un publipostage à partir d'un objet ADO Recordset dans le document avec des régions de publipostage. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Renvoie une collection de noms de champs de publipostage disponibles dans le document. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Renvoie une collection de noms de champs de publipostage disponibles dans la région. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Renvoie une collection de noms de champs de publipostage disponibles dans la région. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Renvoie une collection de régions de publipostage portant le nom spécifié. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Renvoie une hiérarchie complète des régions (avec champs) disponibles dans le document. |

## Remarques

Pour que le publipostage fonctionne, le document doit contenir les champs Word MERGEFIELD et NEXT (facultatif). Lors du publipostage, les champs de fusion du document sont remplacés par les valeurs de votre source de données.

Il existe deux manières distinctes d'utiliser le publipostage : avec des régions de publipostage et sans.

La fusion et le publipostage la plus simple est sans régions et fonctionne de manière très similaire à la fusion et au publipostage dans Word.Exécuter méthodes pour fusionner les informations provenant de certaines sources de données telles que**Table de données** ,**Ensemble de données** ,**Vue des données** ,**IDataReader** ou un tableau d'objets dans votre document. The `MailMerge` l'objet traite tous les enregistrements de la source de données et copie et ajoute le contenu de l'ensemble du document pour chaque enregistrement.

Notez que lorsque`MailMerge`l'objet rencontre un champ SUIVANT, il sélectionne l'enregistrement suivant dans la source de données et continue la fusion sans copier aucun contenu.

Utiliser[`ExecuteWithRegions`](./executewithregions/) et autres surcharges pour fusionner des informations dans un document a avec des zones de publipostage définies. Vous pouvez utiliser **Ensemble de données** ,**Table de données** ,**Vue des données** ou**IDataReader** comme sources de données pour cette opération.

Vous devez utiliser des zones de publipostage pour agrandir dynamiquement des portions du document x000d. Sans zones de publipostage, le document entier sera répété pour chaque enregistrement de la source de données x000d.

## Exemples

Montre comment exécuter un publipostage avec des données provenant d'un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Vous trouverez ci-dessous deux manières d'utiliser un DataTable comme source de données pour un publipostage.
    // 1 - Utilisez la table entière pour le publipostage afin de créer un document de publipostage de sortie pour chaque ligne de la table :
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilisez une ligne du tableau pour créer un document de publipostage de sortie :
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
