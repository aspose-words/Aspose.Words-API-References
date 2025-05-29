---
title: ImageFieldMergingArgs Class
linktitle: ImageFieldMergingArgs
articleTitle: ImageFieldMergingArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.MailMerging.ImageFieldMergingArgs, utformad för att förbättra bildsammanslagning i dokument, vilket säkerställer sömlösa och effektiva arbetsflöden.
type: docs
weight: 4520
url: /sv/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Tillhandahåller data för[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) händelse.

För att lära dig mer, besök[Koppla dokument och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Returnerar[`Document`](../fieldmergingargsbase/document/)objekt för vilket dokumentkopplingen utförs. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Hämtar namnet på kopplingsfältet som anges i dokumentet. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Hämtar objektet som representerar det aktuella kopplingsfältet. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Hämtar namnet på kopplingsfältet i datakällan. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Hämtar eller anger värdet för fältet från datakällan. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | Anger bilden som kopplad dokument måste infoga i dokumentet. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | Anger filnamnet på bilden som kopplingsfunktionen måste infoga i dokumentet. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | Anger bildhöjden för bilden som ska infogas i dokumentet. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | Anger strömmen som kopplingsmotorn ska läsa en bild från. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | Anger bildbredden för bilden som ska infogas i dokumentet. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Hämtar det nollbaserade indexet för posten som sammanfogas. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | Anger den form som kopplad dokument måste infoga i dokumentet. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Hämtar namnet på datatabellen för den aktuella sammanfogningsoperationen eller en tom sträng om namnet inte är tillgängligt. |

## Anmärkningar

Den här händelsen inträffar under dokumentkoppling när ett bildfält för dokumentkoppling påträffas i dokumentet. Du kan svara på den här händelsen för att returnera ett filnamn, en ström eller enImage objektet till mail merge -motorn så att det infogas i dokumentet.

Det finns tre fastigheter tillgängliga[`ImageFileName`](./imagefilename/) , [`ImageStream`](./imagestream/) och[`Image`](./image/) för att ange var bilden måste vara tagen ifrån. Ange endast en av dessa egenskaper.

För att infoga ett bildfält för koppling av dokument i ett dokument i Word, välj Infoga/Fält-kommandot, och välj sedan SammanfogaFält och skriv Bild:MittFältnamn.

## Exempel

Visar hur man infogar bilder som lagras i ett BLOB-fält i en rapport.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Öppna dataläsaren, som måste vara i ett läge som läser alla poster samtidigt.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Gör ingenting.
    }

    /// <summary>
    /// Detta anropas när en dokumentkoppling stöter på ett MERGEFIELD i dokumentet med en "Image:"-tagg i namnet.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)
