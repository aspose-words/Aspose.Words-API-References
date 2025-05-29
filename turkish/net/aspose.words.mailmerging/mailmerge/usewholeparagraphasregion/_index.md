---
title: MailMerge.UseWholeParagraphAsRegion
linktitle: UseWholeParagraphAsRegion
articleTitle: UseWholeParagraphAsRegion
second_title: .NET için Aspose.Words
description: Posta birleştirme bölgelerinizi geliştirmek ve içerik ekleme üzerinde tam kontrol sağlamak için MailMerge UseWholeParagraphAsRegion özelliğini nasıl kullanacağınızı keşfedin.
type: docs
weight: 160
url: /tr/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

Tüm paragrafın bir değerle gösterilip gösterilmediğini belirten bir değer alır veya ayarlar**TabloBaşlangıcı** veya**Tablo Sonu** field veya belirli aralık**TabloBaşlangıcı** Ve**Tablo Sonu** alanlar posta birleştirme bölgesine dahil edilmelidir.

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

## Notlar

Varsayılan değer:`doğru` .

## Örnekler

Posta birleştirme bölgeleri ile paragraflar arasındaki ilişkiyi gösterir.

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // Varsayılan olarak, bir paragraf en fazla birden fazla posta birleştirme bölgesine ait olabilir.
    // Belgemizin içeriği bu ölçütleri karşılamıyor.
    // "UseWholeParagraphAsRegion" bayrağını "true" olarak ayarlarsak,
    // Bu belge üzerinde bir posta birleştirme çalıştırmak bir istisna oluşturacaktır.
    // "UseWholeParagraphAsRegion" bayrağını "false" olarak ayarlarsak,
    // Bu belge üzerinde bir posta birleştirme işlemi gerçekleştirebileceğiz.
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // Posta birleştirme ilk bölgemizi doldururken ikinci bölgeyi kullanılmadan bırakır
    // çünkü kuralı bozan bölge burası.
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// Bir paragrafı paylaşan iki birleştirme bölgesi içeren bir belge oluşturun.
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
/// Bir posta birleştirme sırasında bir bölgeyi doldurabilecek bir veri tablosu oluşturun.
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
