---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: Aspose.Words pour .NET
description: MailMerge MergeDuplicateRegions propriété. Obtient ou définit une valeur indiquant si toutes les régions de publipostage de documents portant le nom dune source de données doivent être fusionnées lors de lexécution dun publipostage avec des régions par rapport à la source de données ou uniquement la première en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Obtient ou définit une valeur indiquant si toutes les régions de publipostage de documents portant le nom d'une source de données doivent être fusionnées lors de l'exécution d'un publipostage avec des régions par rapport à la source de données ou uniquement la première.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

## Exemples

Montre comment travailler avec des régions de publipostage en double.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // Si on définit la propriété "MergeDuplicateRegions" à "false", le publipostage affectera la première région,
    // tandis que les MERGEFIELD du second seront laissés dans l'état de pré-fusion.
    // Pour fusionner les deux régions comme ça,
    // il faudrait exécuter le publipostage deux fois sur une table du même nom.
    // Si nous définissons la propriété "MergeDuplicateRegions" sur "true", le publipostage affectera les deux régions.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Renvoie un document contenant deux régions de publipostage en double (partageant le même nom dans les balises "TableStart/End").
/// </summary>
private static Document CreateSourceDocMergeDuplicateRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column1");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");

    return doc;
}

/// <summary>
/// Crée un tableau de données avec une ligne et deux colonnes.
/// </summary>
private static DataTable CreateSourceTableMergeDuplicateRegions()
{
    DataTable dataTable = new DataTable("MergeRegion");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
