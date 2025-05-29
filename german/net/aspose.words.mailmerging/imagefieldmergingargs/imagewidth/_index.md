---
title: ImageFieldMergingArgs.ImageWidth
linktitle: ImageWidth
articleTitle: ImageWidth
second_title: Aspose.Words für .NET
description: Passen Sie die ImageWidth in ImageFieldMergingArgs an, um Bilder nahtlos in Ihre Dokumente einzufügen und so die visuelle Attraktivität und das Layout zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

Gibt die Bildbreite für das in das Dokument einzufügende Bild an.

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

## Bemerkungen

Der Wert dieser Eigenschaft stammt ursprünglich aus dem entsprechenden MERGEFIELD-Code, der im -Vorlagendokument enthalten ist. Um den ursprünglichen Wert zu überschreiben, sollten Sie eine Instanz von zuweisen.[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) Klasse dieser Eigenschaft oder legen Sie die Eigenschaften für die Instanz von[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) Klasse, die von dieser Eigenschaft zurückgegeben wird.

Um anzugeben, dass der ursprüngliche Wert der Bildbreite angewendet werden soll, sollten Sie den`null` Wert zu dieser Eigenschaft oder setzen Sie den[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) Eigenschaft für die Instanz von[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) Klasse, die von dieser Eigenschaft zurückgegeben wird, auf einen negativen Wert.

## Beispiele

Zeigt, wie die Abmessungen von Bildern festgelegt werden, da MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Fügen Sie ein MERGEFIELD ein, das während eines Serienbriefs Bilder aus einer Quelle akzeptiert. Verwenden Sie den Feldcode zum Verweisen
    // eine Spalte in der Datenquelle, die lokale Systemdateinamen von Bildern enthält, die wir im Serienbrief verwenden möchten.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Die Datenquelle sollte eine solche Spalte mit dem Namen „ImageColumn“ haben.
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Erstellen Sie eine geeignete Datenquelle.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Konfigurieren Sie einen Rückruf, um die Größe der Bilder beim Zusammenführen zu ändern, und führen Sie dann den Seriendruck aus.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Legt die Größe aller Serienbriefbilder auf eine definierte Breite und Höhe fest.
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

### Siehe auch

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
