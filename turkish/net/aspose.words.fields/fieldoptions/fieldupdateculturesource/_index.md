---
title: FieldOptions.FieldUpdateCultureSource
second_title: Aspose.Words for .NET API Referansı
description: FieldOptions mülk. Alan sonucunu biçimlendirmek için hangi kültürün kullanılacağını belirtir.
type: docs
weight: 110
url: /tr/net/aspose.words.fields/fieldoptions/fieldupdateculturesource/
---
## FieldOptions.FieldUpdateCultureSource property

Alan sonucunu biçimlendirmek için hangi kültürün kullanılacağını belirtir.

```csharp
public FieldUpdateCultureSource FieldUpdateCultureSource { get; set; }
```

### Notlar

Varsayılan olarak geçerli iş parçacığının kültürü kullanılır.

Ayar yalnızca \\@ format anahtarına sahip tarih/saat alanlarını etkiler.

### Örnekler

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

* enum [FieldUpdateCultureSource](../../fieldupdateculturesource/)
* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../fieldoptions/)
* toplantı [Aspose.Words](../../../)


