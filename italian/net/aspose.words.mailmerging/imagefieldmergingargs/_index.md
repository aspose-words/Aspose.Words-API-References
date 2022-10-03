---
title: ImageFieldMergingArgs
second_title: Aspose.Words per .NET API Reference
description: Fornisce i dati per ilImageFieldMerging./ifieldmergingcallback/imagefieldmerging/ evento.
type: docs
weight: 3610
url: /it/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Fornisce i dati per il[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) evento.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Restituisce il[`Document`](../fieldmergingargsbase/document/) oggetto per il quale viene eseguita la stampa unione. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Ottiene il nome del campo di unione come specificato nel documento. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Ottiene l'oggetto che rappresenta il campo di unione corrente. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Ottiene il nome del campo di unione nell'origine dati. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Ottiene o imposta il valore del campo dall'origine dati. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | Specifica l'immagine che il motore di stampa unione deve inserire nel documento. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | Imposta il nome file dell'immagine che il motore di stampa unione deve inserire nel documento. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | Specifica l'altezza dell'immagine da inserire nel documento. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | Specifica il flusso da cui il motore di stampa unione deve leggere un'immagine. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | Specifica la larghezza dell'immagine da inserire nel documento. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Ottiene l'indice in base zero del record che viene unito. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | Specifica la forma che il motore di stampa unione deve inserire nel documento. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Ottiene il nome della tabella di dati per l'operazione di unione corrente o una stringa vuota se il nome non è disponibile. |

### Osservazioni

Questo evento si verifica durante la stampa unione quando viene rilevato un campo immagine stampa unione nel documento. Puoi rispondere a questo evento per restituire un nome di file , uno stream o unImage oggetto al motore di stampa unione in modo che venga inserito nel documento.

Sono disponibili tre proprietà[`ImageFileName`](./imagefilename/) , [`ImageStream`](./imagestream/) e[`Image`](./image/) per specificare da dove deve essere presa l'immagine. Impostare solo una di queste proprietà.

Per inserire un campo immagine stampa unione in un documento in Word, seleziona il comando Inserisci/Campo, quindi seleziona UnisciCampo e digita Immagine:MioNomeCampo.

### Esempi

Mostra come inserire in un report le immagini archiviate in un campo BLOB del database.

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

        // Apre il lettore di dati, che deve essere in una modalità che legga tutti i record contemporaneamente.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Fare niente.
    }

    /// <summary>
    /// Viene chiamato quando una stampa unione incontra un MERGEFIELD nel documento con un tag "Image:" nel nome.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

Mostra come impostare le dimensioni delle immagini quando MERGEFIELDS le accetta durante una stampa unione.

```csharp
{
    Document doc = new Document();

    // Inserisce un MERGEFIELD che accetterà immagini da un'origine durante una stampa unione. Utilizzare il codice di campo per fare riferimento
    // una colonna nell'origine dati contenente i nomi dei file di sistema locali delle immagini che desideriamo utilizzare nella stampa unione.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // L'origine dati dovrebbe avere una tale colonna denominata "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Crea un'origine dati adatta.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Configura una richiamata per modificare le dimensioni delle immagini al momento dell'unione, quindi esegui la stampa unione.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// Imposta la dimensione di tutte le immagini unite alla posta su una larghezza e un'altezza definite.
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

### Guarda anche

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
