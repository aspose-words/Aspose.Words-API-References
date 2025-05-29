---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: .NET için Aspose.Words
description: Aspose.Words.MailMerging.MailMerge sınıfıyla güçlü posta birleştirme yeteneklerinin kilidini açın. Belge oluşturmayı kolaylaştırın ve üretkenliği zahmetsizce artırın!
type: docs
weight: 4530
url: /tr/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Posta birleştirme işlevini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Posta Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) belgeleme makalesi.

```csharp
public class MailMerge
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Posta birleştirme sırasında hangi öğelerin kaldırılacağını belirten bir dizi bayrak alır veya ayarlar. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Noktalama işaretli paragrafların boş olarak kabul edilip edilmeyeceğini ve kaldırılıp kaldırılmayacağını belirten bir değer alır veya ayarlar.RemoveEmptyParagraphs seçenek belirtildi. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Belgede bir posta birleştirme alanıyla karşılaşıldığında posta birleştirme sırasında oluşur. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Posta birleştirme sırasında belirli olayların işlenmesine izin verir. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Posta birleştirme işlemi için eşlenen veri alanlarını temsil eden bir koleksiyon döndürür. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Veri kaynağına ait tüm belge birleştirme bölgelerinin, veri kaynağına ait bölgelerle veya yalnızca ilk bölgeyle bir birleştirme işlemi yürütülürken birleştirilip birleştirilmeyeceğini belirten bir değer alır veya ayarlar. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Bölgelerle bir posta birleştirme işlemi yürütülürken tüm belgedeki alanların güncellenip güncellenmeyeceğini belirten bir değer alır veya ayarlar. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Kullanılmayan "mustache" etiketlerinin korunup korunmayacağını belirten bir değer alır veya ayarlar. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Bir posta birleştirme bölgesi son etiketini alır veya ayarlar. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Bir posta birleştirme bölgesi başlangıç etiketini alır veya ayarlar. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Bir posta birleştirmenin yürütülmesinden sonra listelerin her bölümde yeniden başlatılıp başlatılmayacağını belirten bir değer alır veya ayarlar. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Bir değeri alır veya ayarlar.[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) İlk belge bölümünün ve sonraki veri kaynağı satırlarının kopyaları posta birleştirme sırasında saklanır veya MS Word davranışına göre güncellenir. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Posta birleştirme değerlerinden son ve öndeki boşlukların kesilip kesilmeyeceğini belirten bir değer alır veya ayarlar. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Üst IF alanının koşulundan bağımsız olarak birleştirme alanlarının ve birleştirme bölgelerinin birleştirilip birleştirilmeyeceğini belirten bir değer alır veya ayarlar. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Ne zaman`doğru` , MERGEFIELD alanlarına ek olarak, bazı diğer alan türlerinde ve ayrıca "{{fieldName}}" etiketlerinde posta birleştirmenin gerçekleştirildiğini belirtir. |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Tüm paragrafın bir değerle gösterilip gösterilmediğini belirten bir değer alır veya ayarlar**TabloBaşlangıcı** veya**Tablo Sonu** field veya belirli aralık**TabloBaşlangıcı** Ve**Tablo Sonu** alanlar posta birleştirme bölgesine dahil edilmelidir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Belgeden posta birleştirmeyle ilgili alanları kaldırır. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Bir e-posta birleştirme işlemini gerçekleştirir**Veri Satırı** belgeye. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Bir DataTable'dan belgeye posta birleştirme işlemini gerçekleştirir. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Bir e-posta birleştirme işlemini gerçekleştirir**VeriGörünümü** belgeye. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Posta birleştirme işlemini gerçekleştirir**IDataOkuyucu** belgeye. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Özel bir veri kaynağından posta birleştirme gerçekleştirir. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Tek bir kayıt için bir posta birleştirme işlemi gerçekleştirir. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | ADO Kayıt Kümesi nesnesinden belgeye posta birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Bir e-posta birleştirme işlemini gerçekleştirir**Veri Seti** posta birleştirme bölgelerine sahip bir belgeye. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Bir e-posta birleştirme işlemini gerçekleştirir**Veri Tablosu** posta birleştirme bölgeleriyle belgeye. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Bir e-posta birleştirme işlemini gerçekleştirir**VeriGörünümü** posta birleştirme bölgeleriyle belgeye. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Posta birleştirme bölgeleriyle özel bir veri kaynağından posta birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Posta birleştirme bölgeleriyle özel bir veri kaynağından posta birleştirme gerçekleştirir. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Posta birleştirme işlemini gerçekleştirir**IDataOkuyucu** posta birleştirme bölgeleriyle belgeye. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | ADO Kayıt Kümesi nesnesinden belgeye posta birleştirme işlemini posta birleştirme bölgeleriyle gerçekleştirir. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Belgede bulunan birleştirme alanı adlarının bir koleksiyonunu döndürür. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Bölgede kullanılabilen posta birleştirme alanı adlarının bir koleksiyonunu döndürür. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Bölgede kullanılabilen posta birleştirme alanı adlarının bir koleksiyonunu döndürür. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Belirtilen ada sahip bir posta birleştirme bölgeleri koleksiyonu döndürür. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Belgede bulunan bölgelerin (alanlarla birlikte) tam hiyerarşisini döndürür. |

## Notlar

Posta birleştirme işleminin çalışması için, belge Word MERGEFIELD ve isteğe bağlı olarak NEXT alanlarını içermelidir. Posta birleştirme işlemi sırasında, belgedeki birleştirme alanları veri kaynağınızdaki değerlerle değiştirilir.

Posta birleştirmeyi kullanmanın iki farklı yolu vardır: posta birleştirme bölgeleriyle ve bölgesiz.

En basit posta birleştirme, bölgeleri olmayan bir birleştirmedir ve Word'de mail merge 'nin çalışma biçimine çok benzer.Uygulamak bazı veri kaynağından gelen bilgileri birleştirme yöntemleri örneğin**Veri Tablosu** ,**Veri Seti** ,**VeriGörünümü** ,**IDataOkuyucu** veya nesne dizisi belgenize. The `MailMerge` nesnesi veri kaynağının tüm kayıtlarını işler ve her kayıt için tüm belgenin içeriğini kopyalar ve ekler.

Dikkat edin, ne zaman`MailMerge`nesne bir NEXT alanıyla karşılaşırsa, veri kaynağındaki next record öğesini seçer ve herhangi bir içeriği kopyalamadan birleştirmeye devam eder.

Kullanmak[`ExecuteWithRegions`](./executewithregions/) ve bilgileri, posta birleştirme bölgeleri tanımlanmış a belgesine birleştirmek için diğer aşırı yüklemeler. kullanabilirsiniz**Veri Seti** ,**Veri Tablosu** ,**VeriGörünümü** veya**IDataOkuyucu** Bu işlem için veri kaynağı olarak kullanın.

belgesinin içindeki bölümleri dinamik olarak büyütmek istiyorsanız posta birleştirme bölgelerini kullanmanız gerekir. Posta birleştirme bölgeleri olmadan, veri kaynağının her kaydı için tüm belge tekrarlanacaktır.

## Örnekler

DataTable'daki verilerle posta birleştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Aşağıda bir posta birleştirme için veri kaynağı olarak DataTable kullanmanın iki yolu bulunmaktadır.
    // 1 - Tablonun tamamını kullanarak, tablodaki her satır için tek bir çıktı birleştirme belgesi oluşturun:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Tablonun bir satırını kullanarak tek bir çıktı birleştirme belgesi oluşturun:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Bir posta birleştirme kaynak belgesi oluşturur.
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
