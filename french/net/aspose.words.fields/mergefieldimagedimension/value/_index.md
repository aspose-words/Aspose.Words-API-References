---
title: MergeFieldImageDimension.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MergeFieldImageDimension Value pour une gestion optimisée des images. Améliorez votre projet avec des dimensions précises et des performances accrues.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/mergefieldimagedimension/value/
---
## MergeFieldImageDimension.Value property

La valeur.

```csharp
public double Value { get; set; }
```

## Remarques

Vous devez utiliser une valeur négative pour indiquer que la valeur d'origine de la dimension d'image correspondante doit être appliquée.

## Exemples

Montre comment définir les dimensions des images car MERGEFIELDS les accepte lors d'un publipostage.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Insérer un champ MERGEFIELD qui acceptera les images d'une source lors d'un publipostage. Utiliser le code du champ pour référencer
    // une colonne dans la source de données contenant les noms de fichiers système locaux des images que nous souhaitons utiliser dans le publipostage.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // La source de données doit avoir une colonne nommée « ImageColumn ».
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Créez une source de données appropriée.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Configurez un rappel pour modifier les tailles des images au moment de la fusion, puis exécutez le publipostage.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Définit la taille de toutes les images fusionnées sur une largeur et une hauteur définies.
/// </summary>
private class MergedImageResizer : IFieldMergingCallback
{
    public MergedImageResizer(double imageWidth, double imageHeight, MergeFieldImageDimensionUnit unit)
    {
        mImageWidth = imageWidth;
        mImageHeight = imageHeight;
        mUnit = unit;
    }

    public void FieldMerging(FieldMergingArgs e)
    {
        throw new NotImplementedException();
    }

    public void ImageFieldMerging(ImageFieldMergingArgs args)
    {
        args.ImageFileName = args.FieldValue.ToString();
        args.ImageWidth = new MergeFieldImageDimension(mImageWidth, mUnit);
        args.ImageHeight = new MergeFieldImageDimension(mImageHeight, mUnit);

        Assert.AreEqual(mImageWidth, args.ImageWidth.Value);
        Assert.AreEqual(mUnit, args.ImageWidth.Unit);
        Assert.AreEqual(mImageHeight, args.ImageHeight.Value);
        Assert.AreEqual(mUnit, args.ImageHeight.Unit);
        Assert.Null(args.Shape);
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### Voir également

* class [MergeFieldImageDimension](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
