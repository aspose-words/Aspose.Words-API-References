---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété MailMerge MergeWholeDocument met à jour tous les champs lors d'un publipostage basé sur une région, améliorant ainsi l'efficacité et la précision de vos documents.
type: docs
weight: 70
url: /fr/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Obtient ou définit une valeur indiquant si les champs de l'ensemble du document sont mis à jour lors de l'exécution d'un publipostage avec des régions.

```csharp
public bool MergeWholeDocument { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

## Exemples

Affiche la relation entre les fusions de courrier avec les régions et la mise à jour des champs.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // Si nous définissons l'indicateur « MergeWholeDocument » sur « true »,
    // le publipostage avec les régions mettra à jour chaque champ du document.
    // Si nous définissons l'indicateur « MergeWholeDocument » sur « false », le publipostage mettra uniquement à jour les champs
    // dans la région de publipostage dont le nom correspond au nom de la table source de données.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // Le publipostage mettra à jour uniquement le champ QUOTE en dehors de la zone de publipostage
    // si nous définissons l'indicateur "MergeWholeDocument" sur "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// Créez un document avec une région de publipostage appartenant à une source de données nommée « MyTable ».
/// Insérez un champ QUOTE à l'intérieur de cette région et un autre à l'extérieur.
/// </summary>
private static Document CreateSourceDocMergeWholeDocument()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is outside of the \"MyTable\" merge region.";

    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD TableStart:MyTable");

    field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is inside the \"MyTable\" merge region.";
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD MyColumn");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    return doc;
}

/// <summary>
/// Créez une table de données qui sera utilisée dans un publipostage.
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### Voir également

* class [MailMerge](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
