---
title: ImageFieldMergingArgs.ImageWidth
linktitle: ImageWidth
articleTitle: ImageWidth
second_title: Aspose.Words pour .NET
description: ImageFieldMergingArgs ImageWidth propriété. Spécifie la largeur de limage à insérer dans le document en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

Spécifie la largeur de l'image à insérer dans le document.

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

## Remarques

La valeur de cette propriété provient initialement du code du MERGEFIELD correspondant, contenu dans le document modèle . Pour remplacer la valeur initiale, vous devez attribuer une instance de [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) classe à cette propriété ou définissez les propriétés de l'instance de[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) classe, renvoyée par cette propriété.

Pour indiquer que la valeur originale de la largeur de l'image doit être appliquée, vous devez attribuer le`nul` à cette propriété ou définissez la valeur[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) propriété pour l'instance de[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) classe, renvoyée par cette propriété, à une valeur négative.

## Exemples

Montre comment définir les dimensions des images telles que MERGEFIELDS les accepte lors d'un publipostage.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Insère un MERGEFIELD qui acceptera les images d'une source lors d'un publipostage. Utilisez le code de champ pour référencer
    // une colonne dans la source de données contenant les noms de fichiers du système local des images que nous souhaitons utiliser dans le publipostage.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // La source de données doit avoir une telle colonne nommée "ImageColumn".
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
/// Définit la taille de toutes les images fusionnées par courrier sur une largeur et une hauteur définies.
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
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### Voir également

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
