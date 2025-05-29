---
title: Document.FieldOptions
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: .NET için Aspose.Words
description: Alan işlemeyi etkili bir şekilde yönetmek için Belge Alan Seçenekleri özelliğini keşfedin. Gelişmiş belge denetimi ve özelleştirme için benzersiz seçenekleri keşfedin.
type: docs
weight: 130
url: /tr/net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

Bir tane alır[`FieldOptions`](../../../aspose.words.fields/fieldoptions/) belgedeki alan işlemeyi kontrol etme seçeneklerini temsil eden nesne.

```csharp
public FieldOptions FieldOptions { get; }
```

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

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
