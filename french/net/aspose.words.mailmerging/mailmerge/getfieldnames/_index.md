---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words pour .NET
description: Découvrez la méthode MailMerge GetFieldNames pour accéder et utiliser sans effort tous les noms de champs de publipostage de votre document pour une automatisation simplifiée des documents.
type: docs
weight: 220
url: /fr/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Renvoie une collection de noms de champs de publipostage disponibles dans le document.

```csharp
public string[] GetFieldNames()
```

## Remarques

Renvoie les noms de champs de fusion complets, y compris le préfixe facultatif. N'élimine pas les doublons.

Un nouveau tableau de chaînes est créé à chaque appel.

Inclut les noms de champs « moustache » si[`UseNonMergeFields`](../usenonmergefields/) est`vrai`.

## Exemples

Montre comment obtenir les noms de tous les champs de fusion dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Columns.Add("City");
dataTable.Rows.Add(new object[] { "John", "Doe", "New York" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs", "Washington" });

// Pour chaque nom MERGEFIELD dans le document, assurez-vous que la table de données contient une colonne
 // avec le même nom, puis exécutez le publipostage.
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
