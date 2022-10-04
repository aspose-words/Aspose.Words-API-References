---
title: ImageFieldMergingArgs
second_title: Aspose.Words for .NET API Referansı
description: için veri sağlarImageFieldMerging./ifieldmergingcallback/imagefieldmerging/ olay.
type: docs
weight: 3610
url: /tr/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

için veri sağlar[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) olay.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | [`Document`](../fieldmergingargsbase/document/) adres mektup birleştirmenin gerçekleştirildiği nesne. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Belgede belirtildiği gibi birleştirme alanının adını alır. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Geçerli birleştirme alanını temsil eden nesneyi alır. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Veri kaynağındaki birleştirme alanının adını alır. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Veri kaynağından alanın değerini alır veya ayarlar. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | Adres mektup birleştirme motorunun belgeye eklemesi gereken resmi belirtir. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | Adres mektup birleştirme motorunun belgeye eklemesi gereken görüntünün dosya adını ayarlar. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | Resmin belgeye ekleneceği resim yüksekliğini belirtir. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | Adres mektup birleştirme motorunun bir görüntüyü okuması için akışı belirtir. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | Resmin belgeye ekleneceği resim genişliğini belirtir. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Birleştirilmekte olan kaydın sıfır tabanlı dizinini alır. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | Adres mektup birleştirme motorunun belgeye eklemesi gereken şekli belirtir. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Geçerli birleştirme işlemi için veri tablosunun adını veya ad yoksa boş dize adını alır. |

### Notlar

Bu olay, adres mektup birleştirme sırasında belgede bir resim adres mektup birleştirme alanıyla karşılaşıldığında meydana gelir. a dosya adı, akış veya bir dosya adı döndürmek için bu etkinliğe yanıt verebilirsiniz.Image belgeye eklenmesi için adres mektup birleştirme motoruna itiraz edin.

Mevcut üç mülk var[`ImageFileName`](./imagefilename/) , [`ImageStream`](./imagestream/) ve[`Image`](./image/) görüntünün nereden alınması gerektiğini belirtmek için. Bu özelliklerden yalnızca birini ayarlayın.

Word'de bir belgeye görüntü adres mektup birleştirme alanı eklemek için Ekle/Alan komutu, öğesini seçin, ardından MergeField öğesini seçin ve Görüntü:AlanAdı yazın.

### Örnekler

Veritabanı BLOB alanında saklanan görüntülerin bir rapora nasıl ekleneceğini gösterir.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Tüm kayıtları bir kerede okuyan bir modda olması gereken veri okuyucuyu açın.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Hiçbir şey yapma.
    }

    /// <summary>
    /// Adres mektup birleştirme, belgede adında "Image:" etiketi olan bir MERGEFIELD ile karşılaştığında çağrılır.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
