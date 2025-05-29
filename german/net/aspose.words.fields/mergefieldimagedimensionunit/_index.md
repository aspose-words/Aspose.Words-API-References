---
title: MergeFieldImageDimensionUnit Enum
linktitle: MergeFieldImageDimensionUnit
articleTitle: MergeFieldImageDimensionUnit
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Fields.MergeFieldImageDimensionUnit für eine präzise Bildabmessungskontrolle in Serienbriefen. Verbessern Sie noch heute Ihre Dokumentenautomatisierung!
type: docs
weight: 3170
url: /de/net/aspose.words.fields/mergefieldimagedimensionunit/
---
## MergeFieldImageDimensionUnit enumeration

Gibt eine Einheit für die Bildabmessung (also die Breite oder Höhe) an, die in einem Serienbriefprozess verwendet wird.

```csharp
public enum MergeFieldImageDimensionUnit
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Point | `0` | Der Punkt (dh 1/72 Zoll). |
| Percent | `1` | Der Prozentsatz des ursprünglichen Bildabmessungswerts. |

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

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
