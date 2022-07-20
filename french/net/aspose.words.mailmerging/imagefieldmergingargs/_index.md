---
title: ImageFieldMergingArgs
second_title: Référence de l'API Aspose.Words pour .NET
description: Fournit des données pour leImageFieldMerging./ifieldmergingcallback/imagefieldmerging événement.
type: docs
weight: 3610
url: /fr/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Fournit des données pour le[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging) événement.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document) { get; } | Renvoie le[`Document`](../fieldmergingargsbase/document) objet pour lequel le publipostage est effectué. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname) { get; } | Obtient le nom du champ de fusion tel que spécifié dans le document. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field) { get; } | Obtient l'objet qui représente le champ de fusion actuel. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname) { get; } | Obtient le nom du champ de fusion dans la source de données. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue) { get; set; } | Obtient ou définit la valeur du champ à partir de la source de données. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image) { get; set; } | Spécifie l'image que le moteur de publipostage doit insérer dans le document. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename) { get; set; } | Définit le nom de fichier de l'image que le moteur de publipostage doit insérer dans le document. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight) { get; set; } | Spécifie la hauteur de l'image à insérer dans le document. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream) { get; set; } | Spécifie le flux à partir duquel le moteur de publipostage lit une image. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth) { get; set; } | Spécifie la largeur de l'image à insérer dans le document. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex) { get; } | Obtient l'index de base zéro de l'enregistrement en cours de fusion. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape) { get; set; } | Spécifie la forme que le moteur de publipostage doit insérer dans le document. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename) { get; } | Obtient le nom de la table de données pour l'opération de fusion en cours ou une chaîne vide si le nom n'est pas disponible. |

### Remarques

Cet événement se produit lors du publipostage lorsqu'un champ image mail merge est rencontré dans le document. Vous pouvez répondre à cet événement pour renvoyer un nom de fichier, un flux ou unImage objet au moteur de publipostage afin qu'il soit inséré dans le document.

Il y a trois propriétés disponibles[`ImageFileName`](./imagefilename) , [`ImageStream`](./imagestream) et[`Image`](./image) pour spécifier d'où l'image doit être prise. Définissez une seule de ces propriétés.

Pour insérer un champ de fusion et publipostage d'image dans un document dans Word, sélectionnez la commande Insert/Field, puis sélectionnez MergeField et tapez Image:MyFieldName.

### Exemples

Montre comment insérer des images stockées dans un champ BLOB de base de données dans un rapport.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Ouvre le lecteur de données, qui doit être dans un mode qui lit tous les enregistrements à la fois.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Ne fais rien.
    }

    /// <summary>
    /// Ceci est appelé lorsqu'un publipostage rencontre un MERGEFIELD dans le document avec une balise "Image :" dans son nom.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

Montre comment définir les dimensions des images lorsque MERGEFIELDS les accepte lors d'un publipostage.

```csharp
{
    Document doc = new Document();

    // Insère un MERGEFIELD qui acceptera les images d'une source lors d'un publipostage. Utilisez le code de champ pour référencer
    // une colonne dans la source de données contenant les noms de fichiers du système local des images que nous souhaitons utiliser dans le publipostage.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // La source de données doit avoir une telle colonne nommée "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Crée une source de données appropriée.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Configurez un rappel pour modifier la taille des images au moment de la fusion, puis exécutez le publipostage.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// Définit la taille de toutes les images fusionnées par courrier à une largeur et une hauteur définies.
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

* class [FieldMergingArgsBase](../fieldmergingargsbase)
* espace de noms [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
