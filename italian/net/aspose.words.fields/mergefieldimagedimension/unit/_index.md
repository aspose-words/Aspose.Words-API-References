---
title: MergeFieldImageDimension.Unit
second_title: Aspose.Words per .NET API Reference
description: MergeFieldImageDimension proprietà. Lunità.
type: docs
weight: 20
url: /it/net/aspose.words.fields/mergefieldimagedimension/unit/
---
## MergeFieldImageDimension.Unit property

L'unità.

```csharp
public MergeFieldImageDimensionUnit Unit { get; set; }
```

### Esempi

Mostra come impostare le dimensioni delle immagini quando MERGEFIELDS le accetta durante una stampa unione.

```csharp
{
    Document doc = new Document();

    // Inserisce un MERGEFIELD che accetterà immagini da un'origine durante una stampa unione. Utilizzare il codice di campo per fare riferimento
    // una colonna nell'origine dati contenente i nomi dei file di sistema locali delle immagini che desideriamo utilizzare nella stampa unione.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // L'origine dati dovrebbe avere una tale colonna denominata "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Crea un'origine dati adatta.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Configura una richiamata per modificare le dimensioni delle immagini al momento dell'unione, quindi esegui la stampa unione.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// Imposta la dimensione di tutte le immagini unite alla posta su una larghezza e un'altezza definite.
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

### Guarda anche

* enum [MergeFieldImageDimensionUnit](../../mergefieldimagedimensionunit/)
* class [MergeFieldImageDimension](../)
* spazio dei nomi [Aspose.Words.Fields](../../mergefieldimagedimension/)
* assemblea [Aspose.Words](../../../)


