---
title: MailMerge
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente la fonctionnalité de fusion et publipostage.
type: docs
weight: 3620
url: /fr/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Représente la fonctionnalité de fusion et publipostage.

```csharp
public class MailMerge
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions) { get; set; } | Obtient ou définit un ensemble d'indicateurs qui spécifient les éléments à supprimer lors du publipostage. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks) { get; set; } | Obtient ou définit une valeur indiquant si les paragraphes avec des signes de ponctuation sont considérés comme vides et doivent être supprimés si leRemoveEmptyParagraphs l'option est spécifiée. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback) { get; set; } | Se produit pendant le publipostage lorsqu'un champ de publipostage est rencontré dans le document. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback) { get; set; } | Permet de gérer des événements particuliers lors du publipostage. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields) { get; } | Renvoie une collection qui représente les champs de données mappés pour l'opération de fusion et publipostage. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions) { get; set; } | Obtient ou définit une valeur indiquant si toutes les régions de publipostage de document portant le nom d'une source de données doivent être fusionnées lors de l'exécution d'un publipostage avec des régions sur la source de données ou uniquement la première. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument) { get; set; } | Obtient ou définit une valeur indiquant si les champs du document entier sont mis à jour lors de l'exécution d'un publipostage avec des régions. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags) { get; set; } | Obtient ou définit une valeur indiquant si les balises "moustache" inutilisées doivent être conservées. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag) { get; set; } | Obtient ou définit une balise de fin de région de fusion et publipostage. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag) { get; set; } | Obtient ou définit une balise de début de région de fusion et publipostage. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection) { get; set; } | Obtient ou définit une valeur indiquant si les listes sont redémarrées à chaque section après l'exécution d'un publipostage. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart) { get; set; } | Obtient ou définit une valeur indiquant si le[`SectionStart`](../../aspose.words/pagesetup/sectionstart) de la première section de document et ses copies pour les lignes de source de données suivantes sont conservées lors du publipostage ou mises à jour en fonction du comportement de MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces) { get; set; } | Obtient ou définit une valeur indiquant si les espaces de fin et de début sont supprimés des valeurs de publipostage. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions) { get; set; } | Obtient ou définit une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés quelle que soit la condition du champ IF parent. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields) { get; set; } | Lorsqu'il est vrai, spécifie qu'en plus des champs MERGEFIELD, le publipostage est effectué dans d'autres types de champs et également dans les balises "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion) { get; set; } | Obtient ou définit une valeur indiquant si le paragraphe entier avec le champ TableStart ou TableEnd ou une plage particulière entre les champs TableStart et TableEnd doit être inclus dans la région de fusion et publipostage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields)() | Supprime les champs liés au publipostage du document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_1)(DataRow) | Effectue un publipostage à partir d'un DataRow dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_2)(DataTable) | Effectue une fusion et publipostage à partir d'un DataTable dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_3)(DataView) | Effectue un publipostage à partir d'un DataView dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_4)(IDataReader) | Effectue une fusion et publipostage depuis IDataReader dans le document. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute)(IMailMergeDataSource) | Effectue un publipostage à partir d'une source de données personnalisée. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_5)(string[], object[]) | Effectue une opération de fusion et publipostage pour un seul enregistrement. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado)(object) | Effectue une fusion et publipostage à partir d'un objet ADO Recordset dans le document. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_2)(DataSet) | Effectue un publipostage à partir d'un DataSet dans un document avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_3)(DataTable) | Effectue une fusion et publipostage à partir d'un DataTable dans le document avec des régions de fusion et publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_4)(DataView) | Effectue un publipostage à partir d'un DataView dans le document avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions)(IMailMergeDataSource) | Effectue un publipostage à partir d'une source de données personnalisée avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_1)(IMailMergeDataSourceRoot) | Effectue un publipostage à partir d'une source de données personnalisée avec des régions de publipostage. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_5)(IDataReader, string) | Effectue un publipostage depuis IDataReader dans le document avec les régions de publipostage. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado)(object, string) | Effectue une fusion et publipostage à partir d'un objet ADO Recordset dans le document avec des régions de fusion et publipostage. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames)() | Renvoie une collection de noms de champs de publipostage disponibles dans le document. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion#getfieldnamesforregion)(string) | Renvoie une collection de noms de champs de publipostage disponibles dans la région. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion#getfieldnamesforregion_1)(string, int) | Renvoie une collection de noms de champs de publipostage disponibles dans la région. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname)(string) | Renvoie une collection de régions de fusion et publipostage avec le nom spécifié. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy)() | Renvoie une hiérarchie complète des régions (avec champs) disponibles dans le document. |

### Remarques

Pour que l'opération de fusion et publipostage fonctionne, le document doit contenir Word MERGEFIELD et éventuellement les champs NEXT. Lors de l'opération de fusion et publipostage, les champs de fusion du document sont remplacés par les valeurs de votre source de données.

Il existe deux manières distinctes d'utiliser le publipostage : avec et sans les régions de publipostage.

Le publipostage le plus simple est sans régions et il est très similaire au fonctionnement du publipostage dans Word. UtilisationExécuter méthodes pour fusionner des informations à partir d'une source de données some telles que **Tableau de données** , **Base de données** , **Affichage des données** , **IDataReader** ou un tableau d'objets dans votre document. Le  **Publipostage** L'objet traite tous les enregistrements de la source de données et copie et appends le contenu de l'ensemble du document pour chaque enregistrement.

Notez que lorsque **Publipostage**rencontre un champ NEXT, il sélectionne le prochain record dans la source de données et continue la fusion sans copier de contenu.

UtilisationExécuterAvecRégions méthodes pour fusionner des informations dans un document a avec des régions de fusion et publipostage définies. Vous pouvez utiliser  **Base de données** , **Tableau de données** , **Affichage des données** ou **IDataReader** comme sources de données pour cette opération.

Vous devez utiliser des régions de fusion et publipostage si vous souhaitez développer dynamiquement des portions à l'intérieur du document the . Sans régions de fusion et publipostage, le document entier sera répété pour chaque enregistrement de la source de données.

### Exemples

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
    // 1 - Utiliser le tableau entier pour le publipostage afin de créer un document de publipostage de sortie pour chaque ligne du tableau :
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilisez une ligne du tableau pour créer un document de publipostage de sortie :
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crée un document source de fusion et publipostage.
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

* espace de noms [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
