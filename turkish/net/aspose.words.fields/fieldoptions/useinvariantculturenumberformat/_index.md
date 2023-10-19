---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words for .NET
description: FieldOptions UseInvariantCultureNumberFormat mülk. Sayı biçiminin değişmez kültür veya not kullanılarak ayrıştırıldığını belirten değeri alır veya ayarlar C#'da.
type: docs
weight: 210
url: /tr/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Sayı biçiminin değişmez kültür veya not kullanılarak ayrıştırıldığını belirten değeri alır veya ayarlar.

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## Notlar

Bu özellik olarak ayarlandığında`doğru` , sayı formatı değişmez bir kültürden alınmıştır.

Bu özellik olarak ayarlandığında`YANLIŞ` , sayı biçimi geçerli ileti dizisinin kültüründen alınır.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Sayıların değişmez kültüre göre nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // Bazen alanlar belirli kültürlerde sayılarını doğru biçimlendirmeyebilir.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1234567,89 .     ", field.Result);

// Bunu düzeltmek için tüm başlığın kültürünü değiştirebiliriz.
// Bunu düzeltmenin başka bir yolu da bu bayrağı ayarlamaktır,
// sayıları biçimlendirirken tüm alanların değişmez kültürü kullanmasını sağlar.
// Bu şekilde tüm iş parçacığının kültürünü değiştirmekten kaçınmamızı sağlar.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
