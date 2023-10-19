---
title: MailMerge.UseWholeParagraphAsRegion
linktitle: UseWholeParagraphAsRegion
articleTitle: UseWholeParagraphAsRegion
second_title: Aspose.Words for .NET
description: MailMerge UseWholeParagraphAsRegion mülk. Paragrafın tamamının olup olmadığını belirten bir değer alır veya ayarlar.TabloBaşlangıcı veyaTablo Sonu field veya arasındaki belirli aralıkTabloBaşlangıcı VeTablo Sonu alanlar adresmektup birleştirme bölgesine dahil edilmelidir C#'da.
type: docs
weight: 160
url: /tr/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

Paragrafın tamamının olup olmadığını belirten bir değer alır veya ayarlar.**TabloBaşlangıcı** veya**Tablo Sonu** field veya arasındaki belirli aralık**TabloBaşlangıcı** Ve**Tablo Sonu** alanlar adres-mektup birleştirme bölgesine dahil edilmelidir.

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

## Notlar

Varsayılan değer:`doğru` .

## Örnekler

Adres-mektup birleştirme bölgeleri ve paragraflar arasındaki ilişkiyi gösterir.

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // Varsayılan olarak bir paragraf birden fazla adres-mektup birleştirme bölgesine ait olamaz.
    // Dokümanımızın içeriği bu kriterleri karşılamıyor.
    // "UseWholeParagraphAsRegion" bayrağını "true" olarak ayarlarsak,
    // bu belgede adres-mektup birleştirmeyi çalıştırmak bir istisna oluşturacaktır.
    // "UseWholeParagraphAsRegion" bayrağını "false" olarak ayarlarsak,
    // bu belge üzerinde adres-mektup birleştirme işlemi yapabileceğiz.
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // Adres-mektup birleştirme ilk bölgemizi doldururken ikinci bölgeyi kullanılmadan bırakır
    //çünkü kuralı bozan bölgedir.
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// Bir paragrafı paylaşan iki adres-mektup birleştirme bölgesine sahip bir belge oluşturun.
/// </summary>
private static Document CreateSourceDocWithNestedMergeRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Region 1: ");
    builder.InsertField(" MERGEFIELD TableStart:MyTable");
    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    builder.Write(", Region 2: ");
    builder.InsertField(" MERGEFIELD TableStart:MyOtherTable");
    builder.InsertField(" MERGEFIELD TableEnd:MyOtherTable");

    return doc;
}

/// <summary>
/// Adres-mektup birleştirme sırasında bir bölgeyi doldurabilecek bir veri tablosu oluşturun.
/// </summary>
private static DataTable CreateSourceTableDataTableForOneRegion()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
