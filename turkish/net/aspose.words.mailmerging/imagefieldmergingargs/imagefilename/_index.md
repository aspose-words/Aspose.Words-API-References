---
title: ImageFieldMergingArgs.ImageFileName
linktitle: ImageFileName
articleTitle: ImageFileName
second_title: .NET için Aspose.Words
description: Posta birleştirmeleri sırasında belgelerinize zahmetsizce resim eklemek için ImageFieldMergingArgs'da ImageFileName'i ayarlayın. İş akışınızı bugün geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/imagefieldmergingargs/imagefilename/
---
## ImageFieldMergingArgs.ImageFileName property

Posta birleştirme motorunun belgeye eklemesi gereken görüntünün dosya adını ayarlar.

```csharp
public string ImageFileName { get; set; }
```

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

* class [ImageFieldMergingArgs](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
