---
title: Class MergeFieldImageDimension
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.MergeFieldImageDimension klass. Representerar en bilddimension dvs. bredden eller höjden som används i en kopplingsprocess.
type: docs
weight: 2750
url: /sv/net/aspose.words.fields/mergefieldimagedimension/
---
## MergeFieldImageDimension class

Representerar en bilddimension (dvs. bredden eller höjden) som används i en kopplingsprocess.

För att lära dig mer, besök[Arbeta med Fields](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class MergeFieldImageDimension
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor)(double) | Skapar en bilddimensionsinstans med det angivna värdet i poäng. |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor_1)(double, MergeFieldImageDimensionUnit) | Skapar en bilddimensionsinstans med det givna värdet och den givna enheten. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Unit](../../aspose.words.fields/mergefieldimagedimension/unit/) { get; set; } | Enheten. |
| [Value](../../aspose.words.fields/mergefieldimagedimension/value/) { get; set; } | Värdet. |

### Anmärkningar

För att indikera att bilden ska infogas med sin ursprungliga dimension under en sammanslagning, bör du tilldela ett negativt värde till[`Value`](./value/) egenskap.

### Exempel

Visar hur du ställer in dimensionerna för bilder när MERGEFIELDS accepterar dem under en sammanfogning.

```csharp
public void MergeFieldImageDimension()
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
}

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

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


