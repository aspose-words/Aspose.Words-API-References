---
title: MergeFieldImageDimensionUnit Enum
linktitle: MergeFieldImageDimensionUnit
articleTitle: MergeFieldImageDimensionUnit
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Fields.MergeFieldImageDimensionUnit pour un contrôle précis des dimensions des images lors des publipostages. Optimisez l'automatisation de vos documents dès aujourd'hui !
type: docs
weight: 3170
url: /fr/net/aspose.words.fields/mergefieldimagedimensionunit/
---
## MergeFieldImageDimensionUnit enumeration

Spécifie une unité de dimension d'image (c'est-à-dire la largeur ou la hauteur) utilisée dans un processus de publipostage.

```csharp
public enum MergeFieldImageDimensionUnit
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Point | `0` | Le point (c'est-à-dire 1/72 pouce). |
| Percent | `1` | Le pourcentage de la valeur de dimension de l'image d'origine. |

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

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
