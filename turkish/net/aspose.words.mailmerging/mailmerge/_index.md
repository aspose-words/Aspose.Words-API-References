---
title: Class MailMerge
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.MailMerging.MailMerge sınıf. Adresmektup birleştirme işlevini temsil eder.
type: docs
weight: 3840
url: /tr/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Adres-mektup birleştirme işlevini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Adres Mektup Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokümantasyon makalesi.

```csharp
public class MailMerge
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Adres-mektup birleştirme sırasında hangi öğelerin kaldırılması gerektiğini belirten bir dizi işaret alır veya ayarlar. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Noktalama işaretli paragrafların boş olarak kabul edilip edilmeyeceğini ve eğerRemoveEmptyParagraphs seçenek belirtildi. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Adres-mektup birleştirme sırasında belgede adres-mektup birleştirme alanıyla karşılaşıldığında oluşur. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Adres-mektup birleştirme sırasında belirli olayların işlenmesine izin verir. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Adres-mektup birleştirme işlemi için eşlenen veri alanlarını temsil eden bir koleksiyon döndürür. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Veri kaynağına karşı bölgelerle adres-mektup birleştirme yürütülürken, veri kaynağı adına sahip tüm belge adres-mektup birleştirme bölgelerinin mi yoksa yalnızca ilkinin mi birleştirilmesi gerektiğini belirten bir değer alır veya ayarlar. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Bölgelerle adres-mektup birleştirme yürütülürken belgenin tamamındaki alanların güncellenip güncellenmediğini gösteren bir değer alır veya ayarlar. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Kullanılmayan "bıyık" etiketlerinin korunması gerekip gerekmediğini belirten bir değer alır veya ayarlar. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Adres-mektup birleştirme bölgesi bitiş etiketini alır veya ayarlar. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Adres-mektup birleştirme bölgesi başlangıç etiketini alır veya ayarlar. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Adres-mektup birleştirme yürütüldükten sonra her bölümde listelerin yeniden başlatılıp başlatılmayacağını belirten bir değer alır veya ayarlar. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Olup olmadığını belirten bir değer alır veya ayarlar.[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) ilk belge bölümünün ve sonraki veri kaynağı satırları için kopyaları adres-mektup birleştirme sırasında korunur veya MS Word davranışına göre güncellenir. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Adres-mektup birleştirme değerlerinden sondaki ve baştaki boşlukların kırpılıp kırpılmadığını belirten bir değer alır veya ayarlar. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Ana IF alanının durumuna bakılmaksızın birleştirme alanları ve birleştirme bölgelerinin birleştirilip birleştirilmeyeceğini belirten bir değer alır veya ayarlar. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Ne zaman`doğru` MERGEFIELD alanlarına ek olarak diğer bazı alan türlerinde ve ayrıca "{{fieldName}}" etiketlerinde adres-mektup birleştirme işleminin gerçekleştirildiğini belirtir. |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Paragrafın tamamının olup olmadığını belirten bir değer alır veya ayarlar. **TabloBaşlangıcı** veya **Tablo Sonu** field veya arasındaki belirli aralık **TabloBaşlangıcı** Ve **Tablo Sonu** alanlar adres-mektup birleştirme bölgesine dahil edilmelidir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Adres-mektup birleştirmeyle ilgili alanları belgeden kaldırır. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(DataRow) | Adres-mektup birleştirmeyi bir adresten gerçekleştirir. **Veri Satırı** belgeye. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(DataTable) | DataTable'dan belgeye adres-mektup birleştirme gerçekleştirir. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(DataView) | Adres-mektup birleştirmeyi bir adresten gerçekleştirir. **Veri görünümü** belgeye. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(IDataReader) | Adres-mektup birleştirmeyi şuradan gerçekleştirir: **IDataReader** belgeye. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(IMailMergeDataSource) | Özel bir veri kaynağından adres-mektup birleştirme gerçekleştirir. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(string[], object[]) | Tek bir kayıt için adres-mektup birleştirme işlemi gerçekleştirir. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(object) | Bir ADO Recordset nesnesinden belgeye adres-mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(DataSet) | Adres-mektup birleştirmeyi bir adresten gerçekleştirir. **Veri Kümesi** adres-mektup birleştirme bölgeleri olan bir belgeye. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(DataTable) | Adres-mektup birleştirmeyi bir adresten gerçekleştirir. **Veri tablosu** adres-mektup birleştirme bölgelerinin bulunduğu belgeye. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(DataView) | Adres-mektup birleştirmeyi bir adresten gerçekleştirir. **Veri görünümü** adres-mektup birleştirme bölgelerinin bulunduğu belgeye. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(IMailMergeDataSource) | Adres-mektup birleştirme bölgelerine sahip özel bir veri kaynağından adres-mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(IMailMergeDataSourceRoot) | Adres-mektup birleştirme bölgelerine sahip özel bir veri kaynağından adres-mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(IDataReader, string) | Adres-mektup birleştirmeyi şuradan gerçekleştirir: **IDataReader** adres-mektup birleştirme bölgelerinin bulunduğu belgeye. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(object, string) | Bir ADO Recordset nesnesinden adres-mektup birleştirme bölgelerine sahip belgeye adres-mektup birleştirme gerçekleştirir. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Belgede bulunan adres-mektup birleştirme alan adlarının bir koleksiyonunu döndürür. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(string) | Bölgede mevcut olan adres-mektup birleştirme alan adlarının bir koleksiyonunu döndürür. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(string, int) | Bölgede mevcut olan adres-mektup birleştirme alan adlarının bir koleksiyonunu döndürür. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(string) | Belirtilen ada sahip adres-mektup birleştirme bölgelerinin bir koleksiyonunu döndürür. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Belgede bulunan bölgelerin (alanlarla birlikte) tam hiyerarşisini döndürür. |

### Notlar

Adres-mektup birleştirme işleminin çalışması için belgenin Word MERGEFIELD ve isteğe bağlı olarak NEXT alanlarını içermesi gerekir. Adres-mektup birleştirme işlemi sırasında, belgedeki birleştirme alanları are , veri kaynağınızdaki değerlerle değiştirilir.

Adres-mektup birleştirmeyi kullanmanın iki farklı yolu vardır: adres-mektup birleştirme bölgeleri olan ve olmayan.

En basit adres-mektup birleştirme bölgesizdir ve adres-mektup birleştirme 'nin Word'deki çalışma şekline çok benzer. KullanmakUygulamak some veri kaynağındaki bilgileri birleştirme yöntemleri, örneğin **Veri tablosu** , **Veri Kümesi** , **Veri görünümü** , **IDataReader** veya bir dizi nesneyi belgenize ekleyin. The `MailMerge` nesne, veri kaynağının tüm kayıtlarını işler ve her kayıt için belgenin tamamını kopyalayıp extensions içeriğini işler.

Ne zaman olduğunu unutmayın`MailMerge` nesne bir NEXT alanıyla karşılaştığında, veri kaynağındaki sonraki kayıt 'yi seçer ve herhangi bir içeriği kopyalamadan birleştirmeye devam eder.

Kullanmak[`ExecuteWithRegions`](./executewithregions/) ve adres-mektup birleştirme bölgeleri tanımlanmış olarak bilgileri a belgesine birleştirmek için diğer aşırı yüklemeler. kullanabilirsiniz **Veri Kümesi** , **Veri tablosu** , **Veri görünümü** veya **IDataReader** Bu işlem için veri kaynağı olarak .

belgesinin içindeki bölümleri dinamik olarak büyütmek istiyorsanız adres-mektup birleştirme bölgelerini kullanmanız gerekir. Adres-mektup birleştirme bölgeleri olmadan, belgenin tamamı veri kaynağının her kaydı için tekrarlanacaktır.

### Örnekler

DataTable'daki verilerle adres-mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda, adres-mektup birleştirme için veri kaynağı olarak DataTable'ı kullanmanın iki yolu verilmiştir.
    // 1 - Tablodaki her satır için bir çıktı adres-mektup birleştirme belgesi oluşturmak amacıyla adres-mektup birleştirme için tablonun tamamını kullanın:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Bir çıktı adres-mektup birleştirme belgesi oluşturmak için tablonun bir satırını kullanın:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Adres-mektup birleştirme kaynak belgesi oluşturur.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)


