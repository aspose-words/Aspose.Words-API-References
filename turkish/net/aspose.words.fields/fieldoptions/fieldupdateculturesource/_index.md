---
title: FieldOptions.FieldUpdateCultureSource
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: .NET için Aspose.Words
description: FieldUpdateCultureSource özelliğinin, en iyi netlik ve kullanılabilirlik için istenen kültürü belirleyerek alan sonucu biçimlendirmesini nasıl geliştirdiğini keşfedin.
type: docs
weight: 110
url: /tr/net/aspose.words.fields/fieldoptions/fieldupdateculturesource/
---
## FieldOptions.FieldUpdateCultureSource property

Alan sonucunu biçimlendirmek için hangi kültürün kullanılacağını belirtir.

```csharp
public FieldUpdateCultureSource FieldUpdateCultureSource { get; set; }
```

## Notlar

Varsayılan olarak geçerli iş parçacığının kültürü kullanılır.

Ayar yalnızca \\@ biçim anahtarı olan tarih/saat alanlarını etkiler.

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

* enum [FieldUpdateCultureSource](../../fieldupdateculturesource/)
* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
