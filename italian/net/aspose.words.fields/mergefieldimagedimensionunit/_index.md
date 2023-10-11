---
title: Enum MergeFieldImageDimensionUnit
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.MergeFieldImageDimensionUnit enum. Specifica ununità della dimensione di unimmagine ovvero la larghezza o laltezza utilizzata in un processo di stampa unione.
type: docs
weight: 2760
url: /it/net/aspose.words.fields/mergefieldimagedimensionunit/
---
## MergeFieldImageDimensionUnit enumeration

Specifica un'unità della dimensione di un'immagine (ovvero la larghezza o l'altezza) utilizzata in un processo di stampa unione.

```csharp
public enum MergeFieldImageDimensionUnit
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Point | `0` | Il punto (ovvero 1/72 di pollice). |
| Percent | `1` | La percentuale del valore della dimensione dell'immagine originale. |

### Esempi

Mostra come impostare le dimensioni delle immagini poiché MERGEFIELDS le accetta durante una stampa unione.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Inserisci un MERGEFIELD che accetterà le immagini da una fonte durante una stampa unione. Utilizzare il codice di campo come riferimento
    // una colonna nell'origine dati contenente i nomi dei file di sistema locale delle immagini che desideriamo utilizzare nella stampa unione.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // L'origine dati dovrebbe avere una colonna denominata "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Crea un'origine dati adatta.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Configura una richiamata per modificare le dimensioni delle immagini al momento dell'unione, quindi esegue la stampa unione.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Imposta la dimensione di tutte le immagini unite tramite posta su una larghezza e un'altezza definite.
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

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


