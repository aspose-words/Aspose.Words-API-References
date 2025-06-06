---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: Aspose.Words per .NET
description: Scopri come utilizzare ImageFieldMergingArgs per inserire senza problemi immagini nei tuoi documenti, ottenendo un'esperienza di unione di posta ottimizzata.
type: docs
weight: 10
url: /it/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

Specifica l'immagine che il motore di stampa unione deve inserire nel documento.

```csharp
public Image Image { get; set; }
```

## Esempi

Mostra come utilizzare un callback per personalizzare la logica di unione delle immagini.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // Inserisci un MERGEFIELD che accetterà immagini da una sorgente durante una stampa unione. Utilizza il codice di campo per fare riferimento
    // una colonna nell'origine dati che contiene i nomi dei file di sistema locali delle immagini che desideriamo utilizzare nella stampa unione.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // In questo caso, il campo si aspetta che l'origine dati abbia una colonna denominata "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // I nomi dei file possono essere lunghi e se riusciamo a trovare un modo per evitare di memorizzarli nella sorgente dati,
    // potremmo ridurne considerevolmente le dimensioni.
    // Crea un'origine dati che fa riferimento alle immagini utilizzando nomi brevi.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Assegna un callback di unione che contiene tutta la logica che elabora quei nomi,
     // e quindi eseguire la stampa unione.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// Contiene un dizionario che mappa i nomi delle immagini ai nomi dei file del sistema locale che contengono tali immagini.
/// Se un'origine dati di stampa unione utilizza uno dei nomi del dizionario per fare riferimento a un'immagine,
/// questa callback passerà il rispettivo nome file alla destinazione di unione.
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

### Guarda anche

* class [ImageFieldMergingArgs](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
