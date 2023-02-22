---
title: ImageFieldMergingArgs.ImageWidth
second_title: Aspose.Words for .NET API Referansı
description: ImageFieldMergingArgs mülk. Resmin belgeye ekleneceği resim genişliğini belirtir.
type: docs
weight: 50
url: /tr/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

Resmin belgeye ekleneceği resim genişliğini belirtir.

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

### Notlar

Bu özelliğin değeri, başlangıçta, şablon belgesinde bulunan ilgili MERGEFIELD kodundan gelir. Başlangıç değerini geçersiz kılmak için, bir örneği atamanız gerekir.[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) bu özelliğe sınıf veya örnek için özellikleri ayarlayın[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) sınıf, bu özellik tarafından döndürülür.

Görüntü genişliğinin orijinal değerinin uygulanması gerektiğini belirtmek için, **hükümsüz** değerini bu özelliğe ayarlayın veya[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) instance için özellik[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) bu özellik tarafından negatif bir değere döndürülen sınıf.

### Örnekler

Adres mektup birleştirme sırasında MERGEFIELDS tarafından kabul edildiğinden resimlerin boyutlarının nasıl ayarlanacağını gösterir.

```csharp
{
    Document doc = new Document();

    // Adres mektup birleştirme sırasında bir kaynaktan görüntüleri kabul edecek bir MERGEFIELD ekleyin. Referans için alan kodunu kullanın
    // adres mektup birleştirmede kullanmak istediğimiz görüntülerin yerel sistem dosya adlarını içeren veri kaynağındaki bir sütun.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Veri kaynağının "ImageColumn" adında böyle bir sütunu olmalıdır.
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Uygun bir veri kaynağı oluşturun.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Birleştirme sırasında görüntülerin boyutlarını değiştirmek için bir geri arama yapılandırın, ardından adres mektup birleştirmeyi yürütün.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// Tüm postayla birleştirilmiş resimlerin boyutunu, tanımlanmış bir genişlik ve yüksekliğe ayarlar.
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
* ad alanı [Aspose.Words.MailMerging](../../imagefieldmergingargs/)
* toplantı [Aspose.Words](../../../)


