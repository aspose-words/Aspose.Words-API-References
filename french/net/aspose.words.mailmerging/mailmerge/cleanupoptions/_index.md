---
title: MailMerge.CleanupOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: MailMerge propriété. Obtient ou définit un ensemble dindicateurs qui spécifient les éléments qui doivent être supprimés lors du publipostage.
type: docs
weight: 10
url: /fr/net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

Obtient ou définit un ensemble d'indicateurs qui spécifient les éléments qui doivent être supprimés lors du publipostage.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

### Exemples

Montre comment supprimer les paragraphes vides qu’un publipostage peut créer à partir du document de sortie de la fusion.

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

Montre comment supprimer automatiquement les MERGEFIELD qui restent inutilisés lors du publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créer un document avec des MERGEFIELD pour trois colonnes d'une table source de données de publipostage,
// puis crée une table avec seulement deux colonnes dont les noms correspondent à nos MERGEFIELD.
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

// Notre troisième MERGEFIELD référence une colonne "City", qui n'existe pas dans notre source de données.
// Le publipostage laissera les champs tels que celui-ci intacts dans leur état d'avant la fusion.
// La définition de la propriété "CleanupOptions" sur "RemoveUnusedFields" supprimera tous les MERGEFIELD
// qui restent inutilisés lors d'un publipostage pour nettoyer les documents fusionnés.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Voir également

* enum [MailMergeCleanupOptions](../../mailmergecleanupoptions/)
* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../mailmerge/)
* Assemblée [Aspose.Words](../../../)


