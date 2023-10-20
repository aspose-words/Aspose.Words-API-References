---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: Aspose.Words für .NET
description: ImageFieldMergingArgs Image eigendom. Gibt das Bild an das die SerienbriefEngine in das Dokument einfügen muss in C#.
type: docs
weight: 10
url: /de/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

Gibt das Bild an, das die Serienbrief-Engine in das Dokument einfügen muss.

```csharp
public Image Image { get; set; }
```

## Beispiele

Zeigt, wie Sie einen Rückruf verwenden, um die Bildzusammenführungslogik anzupassen.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // Fügen Sie ein MERGEFIELD ein, das während eines Seriendrucks Bilder von einer Quelle akzeptiert. Verwenden Sie den Feldcode als Referenz
    // eine Spalte in der Datenquelle, die lokale Systemdateinamen von Bildern enthält, die wir im Serienbrief verwenden möchten.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // In diesem Fall erwartet das Feld, dass die Datenquelle eine solche Spalte mit dem Namen „ImageColumn“ hat.
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Dateinamen können lang sein, und wenn wir eine Möglichkeit finden, ihre Speicherung in der Datenquelle zu vermeiden,
    // Wir können die Größe erheblich reduzieren.
    // Erstellen Sie eine Datenquelle, die mit Kurznamen auf Bilder verweist.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Weisen Sie einen Zusammenführungsrückruf zu, der die gesamte Logik enthält, die diese Namen verarbeitet.
     // und dann den Serienbrief ausführen.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// Enthält ein Wörterbuch, das Namen von Bildern den lokalen Systemdateinamen zuordnet, die diese Bilder enthalten.
/// Wenn eine Serienbrief-Datenquelle einen der Namen des Wörterbuchs verwendet, um auf ein Bild zu verweisen,
/// Dieser Rückruf übergibt den entsprechenden Dateinamen an das Zusammenführungsziel.
/// </summary>
private class ImageFilenameCallback : IFieldMergingCallback
{
    public ImageFilenameCallback()
    {
        mImageFilenames = new Dictionary<string, string>();
        mImageFilenames.Add("Dark logo", ImageDir + "Logo.jpg");
        mImageFilenames.Add("Transparent logo", ImageDir + "Transparent background logo.png");
    }

    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        throw new NotImplementedException();
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        if (mImageFilenames.ContainsKey(args.FieldValue.ToString()))
        {
            #if NET48 || JAVA
            args.Image = Image.FromFile(mImageFilenames[args.FieldValue.ToString()]);
            #elif NET5_0_OR_GREATER
            args.Image = SKBitmap.Decode(mImageFilenames[args.FieldValue.ToString()]);
            args.ImageFileName = mImageFilenames[args.FieldValue.ToString()];
            #endif
        }

        Assert.NotNull(args.Image);
    }

    private readonly Dictionary<string, string> mImageFilenames;
}
```

### Siehe auch

* class [ImageFieldMergingArgs](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
