---
title: ImageFieldMergingArgs.ImageHeight
linktitle: ImageHeight
articleTitle: ImageHeight
second_title: Aspose.Words for .NET
description: ImageFieldMergingArgs ImageHeight mülk. Belgeye eklenecek görüntünün görüntü yüksekliğini belirtir C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.mailmerging/imagefieldmergingargs/imageheight/
---
## ImageFieldMergingArgs.ImageHeight property

Belgeye eklenecek görüntünün görüntü yüksekliğini belirtir.

```csharp
public MergeFieldImageDimension ImageHeight { get; set; }
```

## Notlar

Bu özelliğin değeri başlangıçta the şablon belgesinde yer alan karşılık gelen MERGEFIELD kodundan gelir. Başlangıç değerini geçersiz kılmak için bir örneğini atamalısınız[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) sınıfını bu özelliğe ayarlayın veya example öğesinin özelliklerini ayarlayın.[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) bu özellik tarafından döndürülen sınıf.

Görüntü yüksekliğinin orijinal değerinin uygulanması gerektiğini belirtmek için`hükümsüz` Bu özelliğe değerini ayarlayın veya[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) example için özellik[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) Bu özellik tarafından döndürülen sınıf negatif bir değere döner.

## Örnekler

Adres-mektup birleştirme sırasında MERGEFIELDS'in kabul ettiği görüntülerin boyutlarının nasıl ayarlanacağını gösterir.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Adres-mektup birleştirme sırasında bir kaynaktan gelen görüntüleri kabul edecek bir MERGEFIELD ekleyin. Referans vermek için alan kodunu kullanın
    // adres-mektup birleştirmede kullanmak istediğimiz görüntülerin yerel sistem dosya adlarını içeren veri kaynağındaki bir sütun.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Veri kaynağında "ImageColumn" adında bir sütun bulunmalıdır.
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Uygun bir veri kaynağı oluşturun.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Birleştirme sırasında görüntülerin boyutlarını değiştirmek için bir geri arama yapılandırın, ardından adres-mektup birleştirmeyi yürütün.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Adres-postayla birleştirilmiş tüm görsellerin boyutunu tanımlanmış tek bir genişliğe ve yüksekliğe ayarlar.
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

### Ayrıca bakınız

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
