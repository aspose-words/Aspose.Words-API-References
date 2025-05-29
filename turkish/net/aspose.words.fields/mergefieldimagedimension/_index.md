---
title: MergeFieldImageDimension Class
linktitle: MergeFieldImageDimension
articleTitle: MergeFieldImageDimension
second_title: .NET için Aspose.Words
description: Posta birleştirmelerinde hassas görüntü boyutlandırma için Aspose.Words.Fields.MergeFieldImageDimension sınıfını keşfedin. Belge otomasyonunuzu bugün geliştirin!
type: docs
weight: 3160
url: /tr/net/aspose.words.fields/mergefieldimagedimension/
---
## MergeFieldImageDimension class

Bir posta birleştirme işleminde kullanılan bir görüntü boyutunu (yani genişliği veya yüksekliği) temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class MergeFieldImageDimension
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor)(*double*) | Belirtilen nokta değerine sahip bir görüntü boyutu örneği oluşturur. |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor_1)(*double, [MergeFieldImageDimensionUnit](../mergefieldimagedimensionunit/)*) | Belirtilen değer ve belirtilen birimle bir görüntü boyutu örneği oluşturur. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Unit](../../aspose.words.fields/mergefieldimagedimension/unit/) { get; set; } | Birim. |
| [Value](../../aspose.words.fields/mergefieldimagedimension/value/) { get; set; } | Değer. |

## Notlar

Posta birleştirme sırasında görüntünün orijinal boyutuyla eklenmesi gerektiğini belirtmek için, öğesine negatif bir değer atamalısınız.[`Value`](./value/) mülk.

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
