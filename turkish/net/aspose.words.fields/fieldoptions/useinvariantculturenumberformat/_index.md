---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: .NET için Aspose.Words
description: Tutarlı veri işleme için değişmez kültürle sayı biçimlendirmesini kolayca yönetmek üzere FieldOptions UseInvariantCultureNumberFormat özelliğini keşfedin.
type: docs
weight: 210
url: /tr/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Sayı biçiminin değişmez kültür kullanılarak ayrıştırıldığını belirten değeri alır veya ayarlar veya not

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## Notlar

Bu özellik şu şekilde ayarlandığında`doğru` sayı biçimi değişmez bir kültürden alınmıştır.

Bu özellik şu şekilde ayarlandığında`YANLIŞ` , sayı biçimi geçerli iş parçacığının kültüründen alınır.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Değişmez kültüre göre sayıların nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // Bazen alanlar, belirli kültürlerde sayılarını doğru biçimde biçimlendiremeyebilir.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1.234.567,89 ,     ", field.Result);

// Bunu düzeltmek için tüm iş parçacığının kültürünü değiştirebiliriz.
// Bunu düzeltmenin bir başka yolu da bu bayrağı ayarlamak,
// sayıları biçimlendirirken değişmez kültürü kullanacak tüm alanları alır.
// Bu şekilde tüm thread için kültürü değiştirmekten kaçınabiliriz.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
