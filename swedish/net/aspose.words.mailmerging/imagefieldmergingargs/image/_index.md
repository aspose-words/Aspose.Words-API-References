---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: Aspose.Words för .NET
description: Upptäck hur du använder ImageFieldMergingArgs för att sömlöst infoga bilder i dina dokument för en elegant dokumentkopplingsupplevelse.
type: docs
weight: 10
url: /sv/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

Anger bilden som kopplad dokument måste infoga i dokumentet.

```csharp
public Image Image { get; set; }
```

## Exempel

Visar hur man använder en återanropsfunktion för att anpassa logik för bildsammanslagning.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // Infoga ett MERGEFIELD som accepterar bilder från en källa under en dokumentkoppling. Använd fältkoden för att referera
    // en kolumn i datakällan som innehåller lokala systemfilnamn för bilder som vi vill använda i dokumentkopplingen.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // I det här fallet förväntar sig fältet att datakällan ska ha en sådan kolumn med namnet "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Filnamn kan vara långa, och om vi kan hitta ett sätt att undvika att lagra dem i datakällan,
    // vi kan minska dess storlek avsevärt.
    // Skapa en datakälla som refererar till bilder med korta namn.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Tilldela en sammanslagningsåteruppringning som innehåller all logik som bearbetar dessa namn,
     // och sedan köra dokumentkopplingen.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// Innehåller en ordbok som mappar namn på bilder till lokala systemfilnamn som innehåller dessa bilder.
/// Om en datakälla för dokumentkoppling använder ett av ordbokens namn för att referera till en bild,
/// denna återanropning skickar respektive filnamn till sammanslagningsdestinationen.
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

### Se även

* class [ImageFieldMergingArgs](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
