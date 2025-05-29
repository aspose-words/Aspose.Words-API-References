---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: .NET için Aspose.Words
description: Belgelerdeki alan işlemeyi optimize etmek, iş akışınızı ve belge yönetimi verimliliğinizi artırmak için Aspose.Words.Fields.FieldOptions sınıfını keşfedin.
type: docs
weight: 2660
url: /tr/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Bir belgedeki alan işlemeyi kontrol etmek için seçenekleri temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public sealed class FieldOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Özel barkod oluşturucuyu alır veya ayarlar. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | x000d_ için bir bibliyografya stili döndüren bir sağlayıcı alır veya ayarlar.[`FieldBibliography`](../fieldbibliography/) Ve[`FieldCitation`](../fieldcitation/) alanlar. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | MS Word yerleşik şablonlarının yollarını alır veya ayarlar. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Alan karşılaştırma ifadeleri değerlendiricisini alır veya ayarlar. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Mevcut kullanıcı bilgilerini alır veya ayarlar. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | \t anahtarı için özel stil ayırıcısını alır veya ayarlar[`FieldToc`](../fieldtoc/) alan. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Varsayılan belge yazarının adını alır veya ayarlar. Yazarın adı yerleşik belge özelliklerinde zaten belirtilmişse, bu seçenek dikkate alınmaz. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Sorgu sonucunu döndüren bir sağlayıcıyı alır veya ayarlar[`FieldDatabase`](../fielddatabase/) alan. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Bir değeri alır veya ayarlar[`FieldIndexFormat`](./fieldindexformat/) bu, x000d_ biçimlendirmesini temsil eder[`FieldIndex`](../fieldindex/) belgedeki alanlar. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Her belirli alan için belirli bir kültür nesnesi döndüren bir sağlayıcı alır veya ayarlar. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Alan sonucunu biçimlendirmek için hangi kültürün kullanılacağını belirtir. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Alır veya ayarlar[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) uygulama |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Alır veya ayarlar[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) uygulama. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Belgenin dosya adını alır veya ayarlar. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Alan güncellemesi sırasında çift yönlü metnin tam olarak desteklenip desteklenmediğini gösteren değeri alır veya ayarlar. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Alanlar için eski (AW 13.10'dan önceki) sayı biçiminin etkin olup olmadığını gösteren değeri alır veya ayarlar. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Alan değerlerini ön işleme tabi tutmak için kültürü alır veya ayarlar. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Alan sonucunun nasıl biçimlendirileceğini kontrol etmenizi sağlar. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Belge tarafından kullanılan şablonun dosya adını alır veya ayarlar. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Yetkili kategorilerinin tablosunu alır veya ayarlar. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Sayı biçiminin değişmez kültür kullanılarak ayrıştırıldığını belirten değeri alır veya ayarlar veya not |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Alan güncellemesi sırasında yanıtlayanı kullanıcı istemlerine göre alır veya ayarlar. |

## Örnekler

Bir alan güncellemesi veya posta birleştirme sırasında tarih biçimlendirme için kullanılan kültürün kaynağının nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Alman yerel ayarına sahip iki birleştirme alanı ekleyin.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Bir değişkendeki orijinal değerini koruyarak geçerli kültürü ABD İngilizcesine ayarlayın.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Bu birleştirme, tarihi biçimlendirmek için geçerli iş parçacığının kültürünü (ABD İngilizcesi) kullanacaktır.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Bir sonraki birleştirmeyi, kültür değerini alan kodundan kaynaklayacak şekilde yapılandırın. Bu kültürün değeri Almanca olacaktır.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// İlk birleştirme sonucu İngilizce biçimlendirilmiş bir tarih içerirken, ikincisi Almancadır.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// İş parçacığının orijinal kültürünü geri yükleyin.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
