---
title: GeneralFormatCollection Class
linktitle: GeneralFormatCollection
articleTitle: GeneralFormatCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.GeneralFormatCollection sınıf. Genel biçimlerin yazılı bir koleksiyonunu temsil eder C#'da.
type: docs
weight: 2650
url: /tr/net/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class

Genel biçimlerin yazılı bir koleksiyonunu temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class GeneralFormatCollection : IEnumerable<GeneralFormat>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.fields/generalformatcollection/count/) { get; } | Koleksiyondaki öğelerin toplam sayısını alır. |
| [Item](../../aspose.words.fields/generalformatcollection/item/) { get; } | Belirtilen dizinde genel bir format alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.fields/generalformatcollection/add/)(*[GeneralFormat](../generalformat/)*) | Koleksiyona genel bir format ekler. |
| [GetEnumerator](../../aspose.words.fields/generalformatcollection/getenumerator/)() | Bir numaralandırıcı nesnesini döndürür. |
| [Remove](../../aspose.words.fields/generalformatcollection/remove/)(*[GeneralFormat](../generalformat/)*) | Belirtilen genel formatın tüm oluşumlarını koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.fields/generalformatcollection/removeat/)(*int*) | Belirtilen dizindeki genel format oluşumunu kaldırır. |

## Örnekler

Alan sonuçlarının nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Hiçbir format uygulanmadan sonucu görüntüleyen bir alan eklemek için bir belge oluşturucu kullanın.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Alanın özelliklerini kullanarak alanın sonucuna bir format uygulayabiliriz.
// Aşağıda bir alanın sonucuna uygulayabileceğimiz üç tür format bulunmaktadır.
// 1 - Sayısal format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Tarih/saat formatı:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Genel format:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Alanın sonucunu orijinal formuna döndürmek için formatlarımızı kaldırabiliriz.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Ayrıca bakınız

* enum [GeneralFormat](../generalformat/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
