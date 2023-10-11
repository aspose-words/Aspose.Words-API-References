---
title: Class MergeFieldImageDimension
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.MergeFieldImageDimension classe. Rappresenta una dimensione dellimmagine ovvero la larghezza o laltezza utilizzata in un processo di stampa unione.
type: docs
weight: 2750
url: /it/net/aspose.words.fields/mergefieldimagedimension/
---
## MergeFieldImageDimension class

Rappresenta una dimensione dell'immagine (ovvero la larghezza o l'altezza) utilizzata in un processo di stampa unione.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class MergeFieldImageDimension
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor)(double) | Crea un'istanza di dimensione immagine con il valore specificato in punti. |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor_1)(double, MergeFieldImageDimensionUnit) | Crea un'istanza di dimensione immagine con il valore e l'unità specificati. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Unit](../../aspose.words.fields/mergefieldimagedimension/unit/) { get; set; } | L'unità. |
| [Value](../../aspose.words.fields/mergefieldimagedimension/value/) { get; set; } | Il valore. |

### Osservazioni

Per indicare che l'immagine deve essere inserita con la sua dimensione originale durante una stampa unione, è necessario assegnare un valore negativo al[`Value`](./value/) proprietà.

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


