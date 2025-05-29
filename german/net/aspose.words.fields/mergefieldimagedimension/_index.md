---
title: MergeFieldImageDimension Class
linktitle: MergeFieldImageDimension
articleTitle: MergeFieldImageDimension
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.MergeFieldImageDimension für präzise Bildgrößen in Serienbriefen. Optimieren Sie Ihre Dokumentenautomatisierung noch heute!
type: docs
weight: 3160
url: /de/net/aspose.words.fields/mergefieldimagedimension/
---
## MergeFieldImageDimension class

Stellt eine Bildabmessung dar (d. h. die Breite oder die Höhe), die in einem Serienbriefprozess verwendet wird.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class MergeFieldImageDimension
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor)(*double*) | Erstellt eine Bilddimensionsinstanz mit dem angegebenen Wert in Punkten. |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor_1)(*double, [MergeFieldImageDimensionUnit](../mergefieldimagedimensionunit/)*) | Erstellt eine Bilddimensionsinstanz mit dem angegebenen Wert und der angegebenen Einheit. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Unit](../../aspose.words.fields/mergefieldimagedimension/unit/) { get; set; } | Die Einheit. |
| [Value](../../aspose.words.fields/mergefieldimagedimension/value/) { get; set; } | Der Wert. |

## Bemerkungen

Um anzugeben, dass das Bild während eines Serienbriefs in seiner ursprünglichen Größe eingefügt werden soll, sollten Sie dem[`Value`](./value/) Eigenschaft.

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
