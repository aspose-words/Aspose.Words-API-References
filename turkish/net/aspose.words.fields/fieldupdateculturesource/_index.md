---
title: FieldUpdateCultureSource Enum
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: .NET için Aspose.Words
description: Aspose.Words.Fields.FieldUpdateCultureSource'u keşfedin. Gelişmiş belge doğruluğu için özelleştirilebilir kültür ayarlarıyla alan güncellemelerini kontrol edin.
type: docs
weight: 2970
url: /tr/net/aspose.words.fields/fieldupdateculturesource/
---
## FieldUpdateCultureSource enumeration

Alan güncellemesi sırasında hangi kültürün kullanılacağını belirtir.

```csharp
public enum FieldUpdateCultureSource
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| CurrentThread | `0` | Alanları güncellemek için geçerli yürütme iş parçacığının kültürü kullanılır. |
| FieldCode | `1` | Dil ayarı aracılığıyla alan biçimlendirme özelliklerinde belirtilen kültür kullanılır. |

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
