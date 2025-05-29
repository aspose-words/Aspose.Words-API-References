---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit ImageFieldMergingArgs nahtlos Bilder in Ihre Dokumente einfügen und so ein reibungsloses Serienbrief-Erlebnis erzielen.
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

Zeigt, wie Sie mithilfe eines Rückrufs die Logik zum Zusammenführen von Bildern anpassen.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // Fügen Sie ein MERGEFIELD ein, das während eines Serienbriefs Bilder aus einer Quelle akzeptiert. Verwenden Sie den Feldcode zum Verweisen
    // eine Spalte in der Datenquelle, die lokale Systemdateinamen von Bildern enthält, die wir im Serienbrief verwenden möchten.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // In diesem Fall erwartet das Feld, dass die Datenquelle eine solche Spalte mit dem Namen „ImageColumn“ hat.
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Dateinamen können lang sein, und wenn wir einen Weg finden, sie nicht in der Datenquelle zu speichern,
    // wir können seine Größe erheblich reduzieren.
    // Erstellen Sie eine Datenquelle, die mit Kurznamen auf Bilder verweist.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Weisen Sie einen Zusammenführungs-Callback zu, der die gesamte Logik enthält, die diese Namen verarbeitet.
        // und führen Sie dann den Serienbrief aus.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// Enthält ein Wörterbuch, das Bildnamen den lokalen Systemdateinamen zuordnet, die diese Bilder enthalten.
/// Wenn eine Serienbrief-Datenquelle einen der Wörterbuchnamen verwendet, um auf ein Bild zu verweisen,
/// Dieser Rückruf übergibt den jeweiligen Dateinamen an das Zusammenführungsziel.
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
            #if NET461_OR_GREATER || JAVA
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
