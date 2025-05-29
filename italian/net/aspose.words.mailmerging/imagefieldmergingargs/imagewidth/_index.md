---
title: ImageFieldMergingArgs.ImageWidth
linktitle: ImageWidth
articleTitle: ImageWidth
second_title: Aspose.Words per .NET
description: Regola ImageWidth in ImageFieldMergingArgs per inserire senza problemi le immagini nei tuoi documenti, migliorandone l'aspetto visivo e il layout.
type: docs
weight: 50
url: /it/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

Specifica la larghezza dell'immagine da inserire nel documento.

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

## Osservazioni

Il valore di questa proprietà deriva inizialmente dal codice del MERGEFIELD corrispondente, contenuto nel documento modello . Per sovrascrivere il valore iniziale, è necessario assegnare un'istanza di [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) classe a questa proprietà o imposta le proprietà per instance di[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) classe, restituita da questa proprietà.

Per indicare che deve essere applicato il valore originale della larghezza dell'immagine, è necessario assegnare`null` valore a questa proprietà o imposta il[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) proprietà per l'istanza di[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) classe, restituita da questa proprietà, a un valore negativo.

## Esempi

Mostra come impostare le dimensioni delle immagini così come vengono accettate da MERGEFIELDS durante una stampa unione.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Inserisci un MERGEFIELD che accetterà immagini da una sorgente durante una stampa unione. Utilizza il codice di campo per fare riferimento
    // una colonna nell'origine dati contenente i nomi dei file di sistema locali delle immagini che desideriamo utilizzare nella stampa unione.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // L'origine dati dovrebbe avere una colonna denominata "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Creare una fonte dati adatta.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Configura un callback per modificare le dimensioni delle immagini al momento dell'unione, quindi esegui la stampa unione.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Imposta la dimensione di tutte le immagini unite su una larghezza e un'altezza definite.
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

### Guarda anche

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
