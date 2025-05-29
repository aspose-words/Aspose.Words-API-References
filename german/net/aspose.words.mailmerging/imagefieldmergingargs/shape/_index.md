---
title: ImageFieldMergingArgs.Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Shape-Eigenschaft von ImageFieldMergingArgs Ihre Serienbriefdokumente verbessert, indem sie das präzise Einfügen von Formen für ein elegantes Erscheinungsbild ermöglicht.
type: docs
weight: 60
url: /de/net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---
## ImageFieldMergingArgs.Shape property

Gibt die Form an, die das Seriendruckmodul in das Dokument einfügen muss.

```csharp
public Shape Shape { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft angegeben ist, ignoriert die Serienbrief-Engine alle anderen Eigenschaften wie[`ImageFileName`](../imagefilename/) oder[`ImageStream`](../imagestream/) und fügt die Form einfach in das Dokument ein.

Verwenden Sie diese Eigenschaft, um den Prozess des Zusammenführens eines Bildserienfelds vollständig zu steuern. Sie können beispielsweise angeben[`WrapType`](../../../aspose.words.drawing/shapebase/wraptype/)oder eine andere Formeigenschaft, um den resultierenden Knoten zu optimieren. Beachten Sie jedoch, dass Sie für die Bereitstellung des Forminhalts verantwortlich sind.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [ImageFieldMergingArgs](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
