---
title: ImageFieldMergingArgs Class
linktitle: ImageFieldMergingArgs
articleTitle: ImageFieldMergingArgs
second_title: .NET için Aspose.Words
description: Belgelerde görüntü birleştirmeyi geliştirmek, kesintisiz ve verimli iş akışları sağlamak için tasarlanmış Aspose.Words.MailMerging.ImageFieldMergingArgs sınıfını keşfedin.
type: docs
weight: 4520
url: /tr/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Şunun için veri sağlar:[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) olay.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Posta Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) belgeleme makalesi.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | şunu döndürür:[`Document`](../fieldmergingargsbase/document/)posta birleştirme işleminin gerçekleştirildiği nesne. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Belgede belirtilen birleştirme alanının adını alır. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Geçerli birleştirme alanını temsil eden nesneyi alır. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Veri kaynağındaki birleştirme alanının adını alır. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Alanın değerini veri kaynağından alır veya ayarlar. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | Posta birleştirme motorunun belgeye eklemesi gereken resmi belirtir. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | Posta birleştirme motorunun belgeye eklemesi gereken görüntünün dosya adını ayarlar. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | Belgeye eklenecek görüntünün yüksekliğini belirtir. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | Posta birleştirme motorunun bir resmi okuyacağı akışı belirtir. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | Belgeye eklenecek görüntünün görüntü genişliğini belirtir. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Birleştirilen kaydın sıfır tabanlı dizinini alır. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | Posta birleştirme motorunun belgeye eklemesi gereken şekli belirtir. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Geçerli birleştirme işlemi için veri tablosunun adını veya ad mevcut değilse boş dizeyi alır. |

## Notlar

Bu olay, belgede bir resim mail merge alanıyla karşılaşıldığında posta birleştirme sırasında gerçekleşir. Bu olaya yanıt vererek a dosya adını, akışını veya birImage nesneyi mail merge motoruna ekler, böylece belgeye eklenir.

Üç adet mülk mevcut[`ImageFileName`](./imagefilename/) , [`ImageStream`](./imagestream/) Ve[`Image`](./image/) Görüntünün nereden alınacağını belirtmek için. Bu özelliklerden yalnızca birini ayarlayın.

Word'deki bir belgeye resim birleştirme alanı eklemek için Ekle/Alan komutunu, seçin, ardından MergeField'ı seçin ve Resim:MyFieldName yazın.

## Örnekler

Bir veritabanı BLOB alanında saklanan görsellerin bir rapora nasıl ekleneceğini gösterir.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Tüm kayıtları aynı anda okuyan bir modda olması gereken veri okuyucusunu açın.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Hiçbir şey yapmayın.
    }

    /// <summary>
    /// Bu, bir posta birleştirme işlemi belgede adında "Image:" etiketi bulunan bir MERGEFIELD ile karşılaştığında çağrılır.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)
