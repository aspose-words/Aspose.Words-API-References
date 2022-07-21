---
title: ImageFieldMergingArgs
second_title: Aspose.Words für .NET-API-Referenz
description: Liefert Daten für dieImageFieldMerging./ifieldmergingcallback/imagefieldmerging Ereignis.
type: docs
weight: 3610
url: /de/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Liefert Daten für die[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging) Ereignis.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document) { get; } | Gibt die zurück[`Document`](../fieldmergingargsbase/document) Objekt, für das der Seriendruck durchgeführt wird. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname) { get; } | Ruft den Namen des Briefvorlagenfelds ab, wie im Dokument angegeben. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field) { get; } | Ruft das Objekt ab, das das aktuelle Briefvorlagenfeld darstellt. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname) { get; } | Ruft den Namen des Briefvorlagenfelds in der Datenquelle ab. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue) { get; set; } | Ruft den Wert des Felds aus der Datenquelle ab oder legt ihn fest. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image) { get; set; } | Gibt das Bild an, das das Serienbriefmodul in das Dokument einfügen muss. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename) { get; set; } | Legt den Dateinamen des Bildes fest, das die Seriendruck-Engine in das Dokument einfügen muss. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight) { get; set; } | Gibt die Bildhöhe für das in das Dokument einzufügende Bild an. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream) { get; set; } | Gibt den Stream an, aus dem die Mail-Merge-Engine ein Bild lesen soll. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth) { get; set; } | Gibt die Bildbreite für das Bild an, das in das Dokument eingefügt werden soll. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex) { get; } | Ruft den nullbasierten Index des Datensatzes ab, der zusammengeführt wird. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape) { get; set; } | Gibt die Form an, die das Serienbriefmodul in das Dokument einfügen muss. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename) { get; } | Ruft den Namen der Datentabelle für den aktuellen Zusammenführungsvorgang oder eine leere Zeichenfolge ab, wenn der Name nicht verfügbar ist. |

### Bemerkungen

Dieses Ereignis tritt während des Seriendrucks auf, wenn ein Bild-Seriendruckfeld im Dokument gefunden wird. Sie können auf dieses Ereignis reagieren, um einen Dateinamen, Stream oder eine zurückzugebenImage -Objekt an die Mailmerge -Engine, damit es in das Dokument eingefügt wird.

Es stehen drei Eigenschaften zur Verfügung[`ImageFileName`](./imagefilename) , [`ImageStream`](./imagestream) und[`Image`](./image) um anzugeben, woher das Bild genommen werden muss. Legen Sie nur eine dieser Eigenschaften fest.

Um ein Bild-Seriendruckfeld in ein Dokument in Word einzufügen, wählen Sie den Befehl Einfügen/Feld, , dann MergeField und geben Sie Image:MyFieldName ein.

### Beispiele

Zeigt, wie in einem Datenbank-BLOB-Feld gespeicherte Bilder in einen Bericht eingefügt werden.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Öffnen Sie den Datenleser, der sich in einem Modus befinden muss, der alle Datensätze auf einmal liest.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Nichts tun.
    }

    /// <summary>
    /// Dies wird aufgerufen, wenn ein Seriendruck auf ein MERGEFIELD im Dokument mit einem "Image:"-Tag im Namen trifft.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

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

* class [FieldMergingArgsBase](../fieldmergingargsbase)
* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
