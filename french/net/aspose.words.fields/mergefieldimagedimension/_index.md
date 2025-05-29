---
title: MergeFieldImageDimension Class
linktitle: MergeFieldImageDimension
articleTitle: MergeFieldImageDimension
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.MergeFieldImageDimension pour un dimensionnement précis des images lors des publipostages. Optimisez l'automatisation de vos documents dès aujourd'hui !
type: docs
weight: 3160
url: /fr/net/aspose.words.fields/mergefieldimagedimension/
---
## MergeFieldImageDimension class

Représente une dimension d'image (c'est-à-dire la largeur ou la hauteur) utilisée dans un processus de publipostage.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class MergeFieldImageDimension
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor)(*double*) | Crée une instance de dimension d'image avec la valeur donnée en points. |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor_1)(*double, [MergeFieldImageDimensionUnit](../mergefieldimagedimensionunit/)*) | Crée une instance de dimension d'image avec la valeur donnée et l'unité donnée. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Unit](../../aspose.words.fields/mergefieldimagedimension/unit/) { get; set; } | L'unité. |
| [Value](../../aspose.words.fields/mergefieldimagedimension/value/) { get; set; } | La valeur. |

## Remarques

Pour indiquer que l'image doit être insérée avec sa dimension d'origine lors d'un publipostage, vous devez attribuer une valeur négative à la[`Value`](./value/) propriété.

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
