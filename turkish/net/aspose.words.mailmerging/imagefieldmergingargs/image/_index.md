---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: .NET için Aspose.Words
description: Belgelerinize kusursuz bir şekilde resim eklemek ve kusursuz bir e-posta birleştirme deneyimi yaşamak için ImageFieldMergingArgs'ı nasıl kullanacağınızı keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

Posta birleştirme motorunun belgeye eklemesi gereken resmi belirtir.

```csharp
public Image Image { get; set; }
```

## Örnekler

Görüntü birleştirme mantığını özelleştirmek için geri aramanın nasıl kullanılacağını gösterir.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // Bir posta birleştirme sırasında bir kaynaktan gelen görüntüleri kabul edecek bir MERGEFIELD ekleyin. Alan kodunu referans olarak kullanın
    // posta birleştirmede kullanmak istediğimiz görsellerin yerel sistem dosya adlarını içeren veri kaynağındaki bir sütun.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Bu durumda, alanın veri kaynağının "ImageColumn" adında bir sütuna sahip olmasını beklemesi gerekir.
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Dosya adları uzun olabilir ve bunları veri kaynağında saklamaktan kaçınmanın bir yolunu bulabilirsek,
    // boyutunu önemli ölçüde küçültebiliriz.
    // Kısa adlar kullanarak resimlere başvuran bir veri kaynağı oluşturun.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Bu adları işleyen tüm mantığı içeren bir birleştirme geri araması atayın,
     // ve ardından posta birleştirmeyi gerçekleştirin.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// Görüntülerin adlarını, bu görüntüleri içeren yerel sistem dosya adlarına eşleyen bir sözlük içerir.
/// Bir posta birleştirme veri kaynağı bir resme atıfta bulunmak için sözlüğün adlarından birini kullanıyorsa,
/// bu geri çağırma, birleştirme hedefine ilgili dosya adını geçirecektir.
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
            #if NET461_OR_GREATER || JAVA
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
