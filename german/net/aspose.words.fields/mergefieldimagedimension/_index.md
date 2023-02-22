---
title: Class MergeFieldImageDimension
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.MergeFieldImageDimension klas. Stellt eine Bildabmessung dh die Breite oder Höhe dar die in einem Seriendruckprozess verwendet wird.
type: docs
weight: 2570
url: /de/net/aspose.words.fields/mergefieldimagedimension/
---
## MergeFieldImageDimension class

Stellt eine Bildabmessung (dh die Breite oder Höhe) dar, die in einem Seriendruckprozess verwendet wird.

```csharp
public class MergeFieldImageDimension
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor)(double) | Erstellt eine Bildabmessungsinstanz mit dem angegebenen Wert in Punkten. |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor_1)(double, MergeFieldImageDimensionUnit) | Erstellt eine Bilddimensionsinstanz mit dem angegebenen Wert und der angegebenen Einheit. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Unit](../../aspose.words.fields/mergefieldimagedimension/unit/) { get; set; } | Die Einheit. |
| [Value](../../aspose.words.fields/mergefieldimagedimension/value/) { get; set; } | Der Wert. |

### Bemerkungen

Um anzugeben, dass das Bild beim Seriendruck mit seiner ursprünglichen Größe eingefügt werden soll, sollten Sie dem einen negativen Wert zuweisen[`Value`](./value/) Eigentum.

### Beispiele

Zeigt, wie die Abmessungen von Bildern festgelegt werden, wenn MERGEFIELDS sie während eines Seriendrucks akzeptiert.

```csharp
{
    Document doc = new Document();

    // Fügen Sie ein MERGEFIELD ein, das Bilder von einer Quelle während eines Seriendrucks akzeptiert. Verwenden Sie den Feldcode zum Verweisen
    // eine Spalte in der Datenquelle, die lokale Systemdateinamen von Bildern enthält, die wir beim Seriendruck verwenden möchten.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Die Datenquelle sollte eine solche Spalte mit dem Namen "ImageColumn" haben.
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Erstellen Sie eine geeignete Datenquelle.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Konfigurieren Sie einen Rückruf, um die Größen von Bildern beim Zusammenführen zu ändern, und führen Sie dann den Seriendruck aus.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// Setzt die Größe aller Serienbilder auf eine definierte Breite und Höhe.
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

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


