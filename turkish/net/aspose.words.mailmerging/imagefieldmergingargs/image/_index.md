---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: Aspose.Words for .NET
description: ImageFieldMergingArgs Image mülk. Adresmektup birleştirme motorunun belgeye eklemesi gereken resmi belirtir C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

Adres-mektup birleştirme motorunun belgeye eklemesi gereken resmi belirtir.

```csharp
public Image Image { get; set; }
```

## Örnekler

Görüntü birleştirme mantığını özelleştirmek için geri aramanın nasıl kullanılacağını gösterir.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // Adres-mektup birleştirme sırasında bir kaynaktan gelen görüntüleri kabul edecek bir MERGEFIELD ekleyin. Referans vermek için alan kodunu kullanın
    // adres-mektup birleştirmede kullanmak istediğimiz görüntülerin yerel sistem dosya adlarını içeren veri kaynağındaki bir sütun.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Bu durumda alan, veri kaynağının "ImageColumn" adında bir sütuna sahip olmasını bekler.
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Dosya adları uzun olabilir ve bunları veri kaynağında saklamaktan kaçınmanın bir yolunu bulabilirsek,
    // boyutunu önemli ölçüde azaltabiliriz.
    // Kısa adlar kullanan görsellere atıfta bulunan bir veri kaynağı oluşturun.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Bu adları işleyen tüm mantığı içeren bir birleştirme geri çağrısı atayın,
     // ve ardından adres-mektup birleştirmeyi yürütün.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// Görüntülerin adlarını, bu görüntüleri içeren yerel sistem dosya adlarıyla eşleştiren bir sözlük içerir.
/// Adres-mektup birleştirme veri kaynağı bir resme atıfta bulunmak için sözlüğün adlarından birini kullanıyorsa,
/// bu geri arama ilgili dosya adını birleştirme hedefine iletecektir.
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
            #if NET48 || JAVA
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

### Ayrıca bakınız

* class [ImageFieldMergingArgs](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
