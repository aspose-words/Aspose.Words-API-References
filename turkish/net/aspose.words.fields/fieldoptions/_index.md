---
title: FieldOptions
second_title: Aspose.Words for .NET API Referansı
description: Bir belgede alan işlemeyi denetleme seçeneklerini temsil eder.
type: docs
weight: 2100
url: /tr/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Bir belgede alan işlemeyi denetleme seçeneklerini temsil eder.

```csharp
public sealed class FieldOptions
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Özel barkod oluşturucuyu alır veya ayarlar. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | MS Word yerleşik şablonlarının yollarını alır veya ayarlar. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Alan karşılaştırma ifadeleri değerlendiricisini alır veya ayarlar. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Geçerli kullanıcı bilgilerini alır veya ayarlar. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | \t anahtarı için özel stil ayırıcı alır veya ayarlar[`FieldToc`](../fieldtoc/) alan. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Varsayılan belge yazarının adını alır veya ayarlar. Yazarın adı yerleşik belge özelliklerinde zaten belirtilmişse, bu seçenek dikkate alınmaz. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | için bir sorgu sonucu döndüren bir sağlayıcı alır veya ayarlar.[`FieldDatabase`](../fielddatabase/) alan. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Alır veya ayarlar[`FieldIndexFormat`](./fieldindexformat/) için biçimlendirmeyi temsil eden[`FieldIndex`](../fieldindex/)belgedeki alanlar. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Her belirli alan için özel bir kültür nesnesi döndüren bir sağlayıcı alır veya ayarlar. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Alan sonucunu biçimlendirmek için hangi kültürün kullanılacağını belirtir. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Alır veya ayarlar[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) uygulama |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Belgenin dosya adını alır veya ayarlar. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Alan güncellemesi sırasında iki yönlü metnin tam olarak desteklenip desteklenmediğini gösteren değeri alır veya ayarlar. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Alanlar için eski (AW 13.10'dan erken) sayı biçiminin etkinleştirilip etkinleştirilmediğini gösteren değeri alır veya ayarlar. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Kültürü alan değerlerini önceden işlemek için alır veya ayarlar. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Alan sonucunun nasıl biçimlendirildiğini kontrol etmenizi sağlar. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Belge tarafından kullanılan şablonun dosya adını alır veya ayarlar. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Yetkili kategorilerinin tablosunu alır veya ayarlar. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Sayı biçiminin değişmez kültür kullanılarak veya değil kullanılarak ayrıştırıldığını belirten değeri alır veya ayarlar |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Alan güncellemesi sırasında yanıtlayanı kullanıcı istemlerine alır veya ayarlar. |

### Örnekler

Alan güncellemesi veya adres mektup birleştirme sırasında tarih biçimlendirmesi için kullanılan kültürün kaynağının nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Almanca yerel ayarıyla iki birleştirme alanı ekleyin.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Bir değişkende orijinal değerini koruduktan sonra geçerli kültürü ABD İngilizcesine ayarlayın.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Bu birleştirme, tarihi biçimlendirmek için geçerli iş parçacığının kültürünü kullanır, ABD İngilizcesi.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Kültür değerini alan kodundan kaynaklamak için sonraki birleştirmeyi yapılandırın. O kültürün değeri Alman olacaktır.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// İlk birleştirme sonucu İngilizce olarak biçimlendirilmiş bir tarih içerirken, ikincisi Almancadır.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// İş parçacığının orijinal kültürünü geri yükleyin.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
