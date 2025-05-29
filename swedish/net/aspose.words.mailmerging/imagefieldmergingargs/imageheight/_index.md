---
title: ImageFieldMergingArgs.ImageHeight
linktitle: ImageHeight
articleTitle: ImageHeight
second_title: Aspose.Words för .NET
description: Ställ in ImageHeight i ImageFieldMergingArgs för att anpassa bildstorleken för ditt dokument, vilket förbättrar visuell attraktionskraft och tydlighet.
type: docs
weight: 30
url: /sv/net/aspose.words.mailmerging/imagefieldmergingargs/imageheight/
---
## ImageFieldMergingArgs.ImageHeight property

Anger bildhöjden för bilden som ska infogas i dokumentet.

```csharp
public MergeFieldImageDimension ImageHeight { get; set; }
```

## Anmärkningar

Värdet för den här egenskapen kommer initialt från motsvarande MERGEFIELD-kod, som finns i malldokumentet . För att åsidosätta det initiala värdet bör du tilldela en instans av [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) klassen till den här egenskapen eller ange egenskaperna för instance av[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) klass, returnerad av denna egenskap.

För att indikera att det ursprungliga värdet för bildhöjden ska tillämpas, bör du tilldela`null` -värdet till den här egenskapen eller ange[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) egenskapen för instance av[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) klass, som returneras av denna egenskap, till ett negativt värde.

## Exempel

Visar hur man ställer in dimensionerna för bilder så som MERGEFIELDS accepterar dem under en dokumentkoppling.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Infoga ett MERGEFIELD som accepterar bilder från en källa under en dokumentkoppling. Använd fältkoden för att referera
    // en kolumn i datakällan som innehåller lokala systemfilnamn för bilder som vi vill använda i dokumentkopplingen.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Datakällan ska ha en sådan kolumn med namnet "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Skapa en lämplig datakälla.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Konfigurera en återanropning för att ändra storleken på bilder vid sammanslagningstillfället och kör sedan dokumentsammanslagningen.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Ställer in storleken på alla kopplade bilder till en definierad bredd och höjd.
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

### Se även

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
