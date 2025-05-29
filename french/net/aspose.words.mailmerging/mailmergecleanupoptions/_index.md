---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.MailMergeCleanupOptions pour gérer efficacement le nettoyage du publipostage. Optimisez vos documents en contrôlant la suppression des éléments de manière transparente.
type: docs
weight: 4540
url: /fr/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

Spécifie les options qui déterminent les éléments supprimés lors du publipostage.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Spécifie une valeur par défaut. |
| RemoveEmptyParagraphs | `1` | Spécifie si les paragraphes qui contenaient des champs de fusion sans données doivent être supprimés du document. Lorsque cette option est définie, les paragraphes qui contiennent des champs de fusion de début et de fin de région qui sont autrement vides sont également supprimés. |
| RemoveUnusedRegions | `2` | Spécifie si les régions de publipostage inutilisées doivent être supprimées du document. |
| RemoveUnusedFields | `4` | Spécifie si les champs de fusion inutilisés doivent être supprimés du document. |
| RemoveContainingFields | `8` | Spécifie si les champs qui contiennent des champs de fusion (par exemple, des IF) doivent être supprimés du document si les champs de fusion imbriqués sont supprimés. |
| RemoveStaticFields | `10` | Indique si les champs statiques doivent être supprimés du document. Les champs statiques sont des champs dont les résultats restent inchangés quelle que soit la modification du document. Les champs dont les résultats ne sont pas stockés dans un document et sont calculés à la volée (commeFieldListNum , FieldSymbol , etc.) ne sont pas considérés comme statiques. |
| RemoveEmptyTableRows | `20` | Spécifie si les lignes vides contenant des régions de publipostage doivent être supprimées du document. |
| RemoveEmptyTables | `40` | Spécifie s'il faut supprimer des tables de documents qui contiennent des régions de publipostage qui ont été supprimées à l'aide de soit leRemoveUnusedRegions ou leRemoveEmptyTableRows option. |

## Exemples

Montre comment supprimer une table vide entière lors du publipostage.

```csharp
DataTable tableCustomers = new DataTable("A");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataSet ds = new DataSet();
ds.Tables.Add(tableCustomers);

Document doc = new Document(MyDir + "Mail merge tables.docx");
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

doc.MailMerge.MergeDuplicateRegions = false;
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyTables | MailMergeCleanupOptions.RemoveUnusedRegions;
doc.MailMerge.ExecuteWithRegions(ds.Tables["A"]);

doc.Save(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");

doc = new Document(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");
Assert.AreEqual(1, doc.GetChildNodes(NodeType.Table, true).Count);
```

Montre comment supprimer les paragraphes vides qu'un publipostage peut créer à partir du document de sortie de fusion.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD TableStart:MyTable");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertField(" MERGEFIELD TableEnd:MyTable");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.ExecuteWithRegions(dataTable);

if (doc.MailMerge.CleanupOptions == MailMergeCleanupOptions.RemoveEmptyParagraphs) 
    Assert.AreEqual(
        "John Doe\r" +
        "Jane Doe", doc.GetText().Trim());
else
    Assert.AreEqual(
        "John Doe\r" +
        " \r" +
        "Jane Doe", doc.GetText().Trim());
```

Montre comment supprimer automatiquement les MERGEFIELD qui ne sont pas utilisés pendant le publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créer un document avec des MERGEFIELD pour trois colonnes d'une table source de données de publipostage,
// puis créez une table avec seulement deux colonnes dont les noms correspondent à nos MERGEFIELD.
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs" });

// Notre troisième MERGEFIELD fait référence à une colonne « Ville », qui n'existe pas dans notre source de données.
// Le publipostage laissera les champs tels que celui-ci intacts dans leur état d'avant la fusion.
// La définition de la propriété « CleanupOptions » sur « RemoveUnusedFields » supprimera tous les MERGEFIELD
// qui ne sont pas utilisés lors d'un publipostage pour nettoyer les documents de fusion.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Voir également

* espace de noms [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../)
