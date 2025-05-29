---
title: ImageFieldMergingArgs Class
linktitle: ImageFieldMergingArgs
articleTitle: ImageFieldMergingArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.MailMerging.ImageFieldMergingArgs, die das Zusammenführen von Bildern in Dokumenten verbessert und nahtlose und effiziente Arbeitsabläufe gewährleistet.
type: docs
weight: 4520
url: /de/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Liefert Daten für die[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) Ereignis.

Um mehr zu erfahren, besuchen Sie die[Serienbriefe und Berichte](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Gibt die[`Document`](../fieldmergingargsbase/document/)Objekt, für das der Serienbrief ausgeführt wird. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Ruft den Namen des Seriendruckfelds ab, wie im Dokument angegeben. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Ruft das Objekt ab, das das aktuelle Seriendruckfeld darstellt. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Ruft den Namen des Seriendruckfelds in der Datenquelle ab. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Ruft den Wert des Felds aus der Datenquelle ab oder legt ihn fest. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | Gibt das Bild an, das die Serienbrief-Engine in das Dokument einfügen muss. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | Legt den Dateinamen des Bildes fest, das die Serienbrief-Engine in das Dokument einfügen muss. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | Gibt die Bildhöhe für das in das Dokument einzufügende Bild an. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | Gibt den Stream an, aus dem die Serienbrief-Engine ein Bild lesen soll. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | Gibt die Bildbreite für das in das Dokument einzufügende Bild an. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Ruft den nullbasierten Index des Datensatzes ab, der zusammengeführt wird. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | Gibt die Form an, die das Seriendruckmodul in das Dokument einfügen muss. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Ruft den Namen der Datentabelle für den aktuellen Zusammenführungsvorgang oder eine leere Zeichenfolge ab, wenn der Name nicht verfügbar ist. |

## Bemerkungen

Dieses Ereignis tritt während des Seriendrucks auf, wenn im Dokument ein Bildfeld „mail merge “ gefunden wird. Sie können auf dieses Ereignis reagieren, um einen „x000d_“-Dateinamen, einen Stream oder eineImage Objekt an die Mail Merge -Engine, damit es in das Dokument eingefügt wird.

Es stehen drei Immobilien zur Verfügung[`ImageFileName`](./imagefilename/) , [`ImageStream`](./imagestream/) Und[`Image`](./image/) um anzugeben, woher das Bild stammen muss. Legen Sie nur eine dieser Eigenschaften fest.

Um ein Serienbrieffeld mit einem Bild in ein Word-Dokument einzufügen, wählen Sie den Befehl „Einfügen/Feld“, , wählen Sie dann „MergeField“ und geben Sie „Image:MyFieldName“ ein.

## Beispiele

Zeigt, wie in einem BLOB-Feld einer Datenbank gespeicherte Bilder in einen Bericht eingefügt werden.

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

        // Öffnen Sie den Datenleser, der sich in einem Modus befinden muss, der alle Datensätze gleichzeitig liest.
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
        // Nichts tun.
    }

    /// <summary>
    /// Dies wird aufgerufen, wenn ein Serienbrief auf ein MERGEFIELD im Dokument trifft, dessen Name ein „Image:“-Tag enthält.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
