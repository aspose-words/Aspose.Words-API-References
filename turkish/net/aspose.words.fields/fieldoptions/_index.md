---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldOptions sınıf. Bir belgedeki alan işlemeyi denetleme seçeneklerini temsil eder C#'da.
type: docs
weight: 2250
url: /tr/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Bir belgedeki alan işlemeyi denetleme seçeneklerini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public sealed class FieldOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Özel barkod oluşturucuyu alır veya ayarlar. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | için kaynakça stili döndüren bir sağlayıcıyı alır veya ayarlar.[`FieldBibliography`](../fieldbibliography/) Ve[`FieldCitation`](../fieldcitation/) alanlar. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | MS Word yerleşik şablonlarının yollarını alır veya ayarlar. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Alan karşılaştırma ifadeleri değerlendiricisini alır veya ayarlar. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Geçerli kullanıcı bilgilerini alır veya ayarlar. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | \t anahtarı için özel stil ayırıcıyı alır veya ayarlar[`FieldToc`](../fieldtoc/) alan. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Varsayılan belge yazarının adını alır veya ayarlar. Yazarın adı yerleşik belge özelliklerinde zaten belirtilmişse, bu seçenek dikkate alınmaz. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Sorgu sonucunu döndüren bir sağlayıcıyı alır veya ayarlar.[`FieldDatabase`](../fielddatabase/) alan. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Bir değeri alır veya ayarlar[`FieldIndexFormat`](./fieldindexformat/) bu, biçimlendirmeyi temsil eder[`FieldIndex`](../fieldindex/) belgedeki alanlar. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Her belirli alana özel bir kültür nesnesi döndüren bir sağlayıcıyı alır veya ayarlar. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Alan sonucunu biçimlendirmek için hangi kültürün kullanılacağını belirtir. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Alır veya ayarlar[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) uygulama |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Alır veya ayarlar[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) uygulama. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Belgenin dosya adını alır veya ayarlar. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Çift yönlü metnin alan güncellemesi sırasında tam olarak desteklenip desteklenmediğini belirten değeri alır veya ayarlar. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Alanlar için eski (AW 13.10 öncesi) sayı biçiminin etkin olup olmadığını belirten değeri alır veya ayarlar. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Alan değerlerini ön işlemek için kültürü alır veya ayarlar. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Alan sonucunun nasıl biçimlendirileceğini kontrol etmeye izin verir. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Belge tarafından kullanılan şablonun dosya adını alır veya ayarlar. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Yetki kategorileri tablosunu alır veya ayarlar. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Sayı biçiminin değişmez kültür veya not kullanılarak ayrıştırıldığını belirten değeri alır veya ayarlar. |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Alan güncellemesi sırasında kullanıcı istemlerine yanıt vereni alır veya ayarlar. |

## Örnekler

Alan güncelleştirmesi veya adres-mektup birleştirme sırasında tarih biçimlendirmesi için kullanılan kültürün kaynağının nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Almanca yerel ayarıyla iki birleştirme alanı ekleyin.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Bir değişkendeki orijinal değerini koruduktan sonra geçerli kültürü ABD İngilizcesine ayarlayın.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Bu birleştirme, tarihi biçimlendirmek için geçerli ileti dizisinin kültürünü (ABD İngilizcesi) kullanacaktır.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Kültür değerini alan kodundan kaynaklamak için bir sonraki birleştirmeyi yapılandırın. O kültürün değeri Alman olacaktır.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// İlk birleştirme sonucu İngilizce olarak biçimlendirilmiş bir tarih içerirken ikincisi Almancadır.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Konunun orijinal kültürünü geri yükleyin.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
