---
title: MailMerge.UseWholeParagraphAsRegion
linktitle: UseWholeParagraphAsRegion
articleTitle: UseWholeParagraphAsRegion
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la propriété MailMerge UseWholeParagraphAsRegion pour améliorer vos régions de publipostage, garantissant un contrôle complet sur l'inclusion du contenu.
type: docs
weight: 160
url: /fr/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

Obtient ou définit une valeur indiquant si le paragraphe entier avec**TableStart** ou**Fin de table** field ou plage particulière entre**TableStart** et**Fin de table** les champs doivent être inclus dans la région de publipostage.

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

## Remarques

La valeur par défaut est`vrai` .

## Exemples

Affiche la relation entre les régions de publipostage et les paragraphes.

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // Par défaut, un paragraphe ne peut appartenir qu'à une seule région de publipostage.
    // Le contenu de notre document ne répond pas à ces critères.
    // Si nous définissons l'indicateur "UseWholeParagraphAsRegion" sur "true",
    // l'exécution d'un publipostage sur ce document générera une exception.
    // Si nous définissons l'indicateur "UseWholeParagraphAsRegion" sur "false",
    // nous pourrons exécuter un publipostage sur ce document.
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // Le publipostage remplit notre première région tout en laissant la deuxième région inutilisée
    // puisque c'est la région qui enfreint la règle.
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// Créez un document avec deux régions de publipostage partageant un paragraphe.
/// </summary>
private static Document CreateSourceDocWithNestedMergeRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Region 1: ");
    builder.InsertField(" MERGEFIELD TableStart:MyTable");
    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    builder.Write(", Region 2: ");
    builder.InsertField(" MERGEFIELD TableStart:MyOtherTable");
    builder.InsertField(" MERGEFIELD TableEnd:MyOtherTable");

    return doc;
}

/// <summary>
/// Créez une table de données pouvant remplir une région lors d'un publipostage.
/// </summary>
private static DataTable CreateSourceTableDataTableForOneRegion()
{
    DataTable dataTable = new DataTable("MyTable");
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
