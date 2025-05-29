---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser ImageFieldMergingArgs pour insérer de manière transparente des images dans vos documents pour une expérience de publipostage soignée.
type: docs
weight: 10
url: /fr/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

Spécifie l'image que le moteur de publipostage doit insérer dans le document.

```csharp
public Image Image { get; set; }
```

## Exemples

Montre comment utiliser un rappel pour personnaliser la logique de fusion d'images.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // Insérer un champ MERGEFIELD qui acceptera les images d'une source lors d'un publipostage. Utiliser le code du champ pour référencer
    // une colonne dans la source de données qui contient les noms de fichiers système locaux des images que nous souhaitons utiliser dans le publipostage.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Dans ce cas, le champ s'attend à ce que la source de données ait une colonne nommée « ImageColumn ».
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Les noms de fichiers peuvent être longs, et si nous pouvons trouver un moyen d'éviter de les stocker dans la source de données,
    // nous pouvons réduire considérablement sa taille.
    // Créez une source de données qui fait référence aux images à l'aide de noms courts.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Attribuer un rappel de fusion qui contient toute la logique qui traite ces noms,
     // puis exécutez le publipostage.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// Contient un dictionnaire qui mappe les noms des images aux noms de fichiers du système local qui contiennent ces images.
/// Si une source de données de publipostage utilise l'un des noms du dictionnaire pour faire référence à une image,
/// ce rappel transmettra le nom de fichier respectif à la destination de fusion.
/// </summary>
private class ImageFilenameCallback : IFieldMergingCallback
{
    public ImageFilenameCallback()
    {
        mImageFilenames = new Dictionary<string, string>();
        mImageFilenames.Add("Dark logo", ImageDir + "Logo.jpg");
        mImageFilenames.Add("Transparent logo", ImageDir + "Transparent background logo.png");
    }

    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        throw new NotImplementedException();
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        if (mImageFilenames.ContainsKey(args.FieldValue.ToString()))
        {
            #if NET461_OR_GREATER || JAVA
            args.Image = Image.FromFile(mImageFilenames[args.FieldValue.ToString()]);
            #elif NET5_0_OR_GREATER
            args.Image = SKBitmap.Decode(mImageFilenames[args.FieldValue.ToString()]);
            args.ImageFileName = mImageFilenames[args.FieldValue.ToString()];
            #endif
        }

        Assert.NotNull(args.Image);
    }

    private readonly Dictionary<string, string> mImageFilenames;
}
```

### Voir également

* class [ImageFieldMergingArgs](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
