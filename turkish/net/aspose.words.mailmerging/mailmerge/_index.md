---
title: Class MailMerge
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.MailMerging.MailMerge sınıf. Adres mektup birleştirme işlevini temsil eder.
type: docs
weight: 3620
url: /tr/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Adres mektup birleştirme işlevini temsil eder.

```csharp
public class MailMerge
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Adres mektup birleştirme sırasında hangi öğelerin kaldırılması gerektiğini belirten bir bayrak kümesi alır veya ayarlar. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Noktalama işaretli paragrafların boş olarak kabul edilip edilmediğini ve aşağıdaki durumlarda kaldırılması gerektiğini belirten bir değer alır veya ayarlar.RemoveEmptyParagraphs seçenek belirtildi. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Adres-mektup birleştirme sırasında belgede bir adres mektup birleştirme alanıyla karşılaşıldığında oluşur. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Adres mektup birleştirme sırasında belirli olayların işlenmesine izin verir. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Adres mektup birleştirme işlemi için eşlenmiş veri alanlarını temsil eden bir koleksiyon döndürür. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Veri kaynağı adına sahip belge adres mektup birleştirme bölgelerinin tümünün, veri kaynağına karşı bölgelerle adres mektup birleştirme yürütülürken mi yoksa yalnızca birinci bölgeyle mi birleştirileceğini belirten bir değer alır veya ayarlar. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Bölgelerle adres mektup birleştirme yürütülürken tüm belgedeki alanların güncellenip güncellenmediğini gösteren bir değer alır veya ayarlar. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Kullanılmayan "bıyık" etiketlerinin korunması gerekip gerekmediğini belirten bir değer alır veya ayarlar. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Adres mektup birleştirme bölgesi bitiş etiketi alır veya ayarlar. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Adres mektup birleştirme bölgesi başlangıç etiketi alır veya ayarlar. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Adres mektup birleştirme yürütüldükten sonra her bölümde listelerin yeniden başlatılıp başlatılmayacağını belirten bir değer alır veya ayarlar. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | olup olmadığını gösteren bir değer alır veya ayarlar.[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) ilk belge bölümünün ve sonraki veri kaynağı satırları için kopyaları adres mektup birleştirme sırasında tutulur veya MS Word davranışına göre güncellenir. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Sondaki ve baştaki boşlukların adres mektup birleştirme değerlerinden kesilip kesilmediğini belirten bir değer alır veya ayarlar. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Üst EĞER alanının koşulundan bağımsız olarak birleştirme alanlarının ve birleştirme bölgelerinin birleştirilip birleştirilmediğini gösteren bir değer alır veya ayarlar. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Doğru olduğunda, MERGEFIELD alanlarına ek olarak, adres mektup birleştirmenin diğer bazı alan türlerinde ve 'nin ayrıca "{{fieldName}}" etiketlerinde gerçekleştirildiğini belirtir. |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | TableStart veya TableEnd field ile tüm paragrafın mı yoksa TableStart ve TableEnd alanları arasındaki belirli aralığın adres mektup birleştirme bölgesine dahil edilip edilmeyeceğini belirten bir değer alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Adres mektup birleştirme ile ilgili alanları belgeden kaldırır. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(DataRow) | Bir DataRow'dan belgeye adres mektup birleştirme gerçekleştirir. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(DataTable) | Bir DataTable'dan belgeye adres mektup birleştirme gerçekleştirir. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(DataView) | Bir DataView'den belgeye adres mektup birleştirme gerçekleştirir. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(IDataReader) | IDataReader'dan belgeye adres mektup birleştirme gerçekleştirir. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(IMailMergeDataSource) | Özel bir veri kaynağından adres mektup birleştirme gerçekleştirir. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(string[], object[]) | Tek bir kayıt için adres mektup birleştirme işlemi gerçekleştirir. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(object) | Bir ADO Recordset nesnesinden belgeye adres mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(DataSet) | Bir DataSet'ten adres mektup birleştirme bölgeleri olan bir belgeye adres mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(DataTable) | Adres mektup birleştirme bölgeleri olan bir DataTable'dan belgeye adres mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(DataView) | Adres-mektup birleştirme bölgeleri olan bir DataView'den belgeye adres mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(IMailMergeDataSource) | Adres mektup birleştirme bölgelerine sahip özel bir veri kaynağından adres mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(IMailMergeDataSourceRoot) | Adres mektup birleştirme bölgelerine sahip özel bir veri kaynağından adres mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(IDataReader, string) | Adres mektup birleştirme bölgeleriyle IDataReader'dan belgeye adres mektup birleştirme gerçekleştirir. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(object, string) | Bir ADO Recordset nesnesinden adres mektup birleştirme bölgeleriyle belgeye adres mektup birleştirme gerçekleştirir. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Belgede bulunan adres mektup birleştirme alan adlarının bir koleksiyonunu döndürür. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(string) | Bölgede kullanılabilen adres mektup birleştirme alan adlarının bir koleksiyonunu döndürür. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(string, int) | Bölgede kullanılabilen adres mektup birleştirme alan adlarının bir koleksiyonunu döndürür. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(string) | Belirtilen ada sahip adres mektup birleştirme bölgeleri koleksiyonunu döndürür. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Belgede bulunan bölgelerin (alanlarla birlikte) tam hiyerarşisini döndürür. |

### Notlar

Adres mektup birleştirme işleminin çalışması için belgede Word MERGEFIELD ve isteğe bağlı olarak NEXT alanları bulunmalıdır. Adres mektup birleştirme işlemi sırasında, belgedeki birleştirme alanları, veri kaynağınızdaki değerlerle değiştirilir .

Adres mektup birleştirmeyi kullanmanın iki farklı yolu vardır: adres mektup birleştirme bölgeleriyle ve olmadan.

En basit adres mektup birleştirme, bölge içermez ve Word'de adres mektup birleştirme 'nin nasıl çalıştığına çok benzer. KullanmakUygulamak gibi bazı veri kaynağından bilgileri birleştirme yöntemleri **Veri tablosu** , **Veri Kümesi** , **Veri görünümü** , **IDataOkuyucu** veya bir dizi nesneyi belgenize ekleyin. the  **Posta birleştirme** nesne, veri kaynağının tüm kayıtlarını işler ve her kayıt için tüm belgenin içeriğini kopyalar ve ekler .

Dikkat edin **Posta birleştirme**nesne bir NEXT alanıyla karşılaşırsa, veri kaynağında sonraki record öğesini seçer ve herhangi bir içeriği kopyalamadan birleştirmeye devam eder.

KullanmakExecuteWithRegions tanımlı adres mektup birleştirme bölgeleriyle bilgileri a belgesinde birleştirme yöntemleri. kullanabilirsiniz **Veri Kümesi** , **Veri tablosu** , **Veri görünümü** veya **IDataOkuyucu** bu işlem için veri kaynakları olarak.

belgesi içindeki bölümleri dinamik olarak büyütmek istiyorsanız adres mektup birleştirme bölgelerini kullanmanız gerekir. Adres mektup birleştirme bölgeleri olmadan, veri kaynağının her kaydı için tüm belge tekrarlanacaktır.

### Örnekler

DataTable'daki verilerle adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda, adres mektup birleştirme için veri kaynağı olarak bir DataTable kullanmanın iki yolu bulunmaktadır.
    // 1 - Tablodaki her satır için bir çıktı adres mektup birleştirme belgesi oluşturmak üzere adres mektup birleştirme için tüm tabloyu kullanın:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Bir çıktı adres mektup birleştirme belgesi oluşturmak için tablonun bir satırını kullanın:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Adres mektup birleştirme kaynak belgesi oluşturur.
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


