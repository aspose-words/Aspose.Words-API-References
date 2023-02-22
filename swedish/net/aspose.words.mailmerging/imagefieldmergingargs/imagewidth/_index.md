---
title: ImageFieldMergingArgs.ImageWidth
second_title: Aspose.Words för .NET API Referens
description: ImageFieldMergingArgs fast egendom. Anger bildbredden för bilden som ska infogas i dokumentet.
type: docs
weight: 50
url: /sv/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

Anger bildbredden för bilden som ska infogas i dokumentet.

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

### Anmärkningar

Värdet på den här egenskapen kommer initialt från motsvarande MERGEFIELDs kod, som finns i malldokumentet . För att åsidosätta det initiala värdet bör du tilldela en instans av [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) klass till den här egenskapen eller ställ in egenskaperna för instans av[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) klass, returneras av den här egenskapen.

För att indikera att det ursprungliga värdet för bildbredden ska tillämpas, bör du tilldela **null** värde till den här egenskapen eller ställ in[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) egenskap för instans av[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) klass, som returneras av den här egenskapen, till ett negativt värde.

### Exempel

Visar hur du ställer in dimensionerna för bilder när MERGEFIELDS accepterar dem under en sammanfogning.

```csharp
{
    Document doc = new Document();

    // Infoga ett MERGEFIELD som kommer att acceptera bilder från en källa under en e-postkoppling. Använd fältkoden för att referera
    // en kolumn i datakällan som innehåller lokala systemfilnamn för bilder som vi vill använda i kopplingen.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Datakällan bör ha en sådan kolumn med namnet "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Skapa en lämplig datakälla.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Konfigurera en återuppringning för att ändra storleken på bilder vid sammanfogning och kör sedan sammankopplingen.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// Ställer in storleken på alla sammanslagna bilder till en definierad bredd och höjd.
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

### Se även

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* namnutrymme [Aspose.Words.MailMerging](../../imagefieldmergingargs/)
* hopsättning [Aspose.Words](../../../)


