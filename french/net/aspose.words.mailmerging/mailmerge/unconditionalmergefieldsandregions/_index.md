---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words pour .NET
description: MailMerge UnconditionalMergeFieldsAndRegions propriété. Obtient ou définit une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés quelle que soit la condition du champ IF parent en C#.
type: docs
weight: 140
url: /fr/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Obtient ou définit une valeur indiquant si les champs de fusion et les régions de fusion sont fusionnés quelle que soit la condition du champ IF parent.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

## Exemples

Montre comment fusionner des champs ou des régions quelle que soit la condition du champ IF parent.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un MERGEFIELD imbriqué dans un champ IF.
// Puisque l'instruction du champ IF est fausse, elle n'affichera pas le résultat du MERGEFIELD.
// Le MERGEFIELD ne recevra également aucune donnée lors d'un publipostage.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// Si nous définissons le flag "UnconditionalMergeFieldsAndRegions" à "true",
// notre publipostage insérera des données dans des champs non affichés tels que notre MERGEFIELD ainsi que tous les autres.
// Si nous mettons le flag "UnconditionalMergeFieldsAndRegions" à "false",
// notre publipostage n'insérera pas de données dans les MERGEFIELD masqués par les champs IF avec de fausses déclarations.
doc.MailMerge.UnconditionalMergeFieldsAndRegions = countAllMergeFields;

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FullName");
dataTable.Rows.Add("James Bond");

doc.MailMerge.Execute(dataTable);

doc.Save(ArtifactsDir + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

Assert.AreEqual(
    countAllMergeFields
        ? "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015"
        : "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.GetText().Trim());
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
