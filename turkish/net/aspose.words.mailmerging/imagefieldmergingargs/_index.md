---
title: Class ImageFieldMergingArgs
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.MailMerging.ImageFieldMergingArgs sınıf. Şunun için veri sağlarImageFieldMerging olay.
type: docs
weight: 3830
url: /tr/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Şunun için veri sağlar:[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) olay.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Adres Mektup Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokümantasyon makalesi.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Şunu döndürür:[`Document`](../fieldmergingargsbase/document/) Adres-mektup birleştirmenin gerçekleştirildiği nesne. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Belgede belirtildiği gibi birleştirme alanının adını alır. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Geçerli birleştirme alanını temsil eden nesneyi alır. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Veri kaynağındaki birleştirme alanının adını alır. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Alanın değerini veri kaynağından alır veya ayarlar. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | Adres-mektup birleştirme motorunun belgeye eklemesi gereken resmi belirtir. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | Adres-mektup birleştirme motorunun belgeye eklemesi gereken resmin dosya adını ayarlar. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | Belgeye eklenecek görüntünün görüntü yüksekliğini belirtir. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | Adres-mektup birleştirme motorunun bir görüntüyü okuyacağı akışı belirtir. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | Belgeye eklenecek görüntünün görüntü genişliğini belirtir. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Birleştirilecek kaydın sıfır tabanlı dizinini alır. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | Adres-mektup birleştirme motorunun belgeye eklemesi gereken şekli belirtir. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Geçerli birleştirme işlemi için veri tablosunun adını veya ad mevcut değilse boş dizeyi alır. |

### Notlar

Bu olay, adres-mektup birleştirme sırasında, belgede bir resim adres-mektup birleştirme alanıyla karşılaşıldığında meydana gelir. a dosya adını, akışını veya bir akışını döndürmek için bu etkinliğe yanıt verebilirsiniz.Image adres-mektup birleştirme motoruna itiraz ederek belgeye eklenmesini sağlayın.

Üç mülk mevcut[`ImageFileName`](./imagefilename/) , [`ImageStream`](./imagestream/) Ve[`Image`](./image/) görüntünün nereden alınması gerektiğini belirtmek için. Bu özelliklerden yalnızca birini ayarlayın.

Word'deki bir belgeye resim adres-mektup birleştirme alanı eklemek için Ekle/Alan komutunu seçin, ardından MergeField'ı seçin ve Resim:AlanAdım yazın.

### Örnekler

Veritabanı BLOB alanında saklanan görüntülerin bir rapora nasıl ekleneceğini gösterir.

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

        // Tüm kayıtları aynı anda okuyacak modda olması gereken veri okuyucuyu açın.
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
        // Hiçbir şey yapma.
    }

    /// <summary>
    /// Adres-mektup birleştirme, belgede adında "Image:" etiketi bulunan bir MERGEFIELD ile karşılaştığında çağrılır.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)


