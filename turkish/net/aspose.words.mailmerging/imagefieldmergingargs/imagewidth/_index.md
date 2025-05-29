---
title: ImageFieldMergingArgs.ImageWidth
linktitle: ImageWidth
articleTitle: ImageWidth
second_title: .NET için Aspose.Words
description: Belgelerinize görselleri sorunsuz bir şekilde eklemek, görsel çekiciliği ve düzeni geliştirmek için ImageFieldMergingArgs'daki ImageWidth'i ayarlayın.
type: docs
weight: 50
url: /tr/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

Belgeye eklenecek görüntünün görüntü genişliğini belirtir.

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

## Notlar

Bu özelliğin değeri başlangıçta, şablon belgesinde bulunan ilgili MERGEFIELD kodundan gelir. Başlangıç değerini geçersiz kılmak için, örneğini atamalısınız[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) bu özelliğe sınıf ekleyin veya instance için özellikleri ayarlayın[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) sınıf, bu özellik tarafından döndürülür.

Görüntü genişliğinin orijinal değerinin uygulanması gerektiğini belirtmek için,`hükümsüz` Bu özelliğe değerini ayarlayın veya[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) instance için özellik[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) Bu özellik tarafından döndürülen sınıf, negatif bir değere.

## Örnekler

MERGEFIELDS'in posta birleştirme sırasında kabul ettiği şekilde resimlerin boyutlarının nasıl ayarlanacağını gösterir.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Bir posta birleştirme sırasında bir kaynaktan gelen görüntüleri kabul edecek bir MERGEFIELD ekleyin. Alan kodunu referans olarak kullanın
    // posta birleştirmede kullanmak istediğimiz görsellerin yerel sistem dosya adlarını içeren veri kaynağındaki bir sütun.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Veri kaynağında "ImageColumn" adında böyle bir sütun bulunmalıdır.
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Uygun bir veri kaynağı oluşturun.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Birleştirme sırasında resimlerin boyutlarını değiştirmek için bir geri arama yapılandırın, ardından posta birleştirmeyi yürütün.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Birleştirilen tüm resimlerin boyutunu tek bir tanımlanmış genişliğe ve yüksekliğe ayarlar.
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

### Ayrıca bakınız

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
