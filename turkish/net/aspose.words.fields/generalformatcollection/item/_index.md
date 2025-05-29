---
title: GeneralFormatCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: Herhangi bir dizinde özelleştirilebilir biçimleri kolayca almak için GeneralFormatCollection Öğesi özelliğine erişin ve verilerinizin sunumunu zahmetsizce geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/generalformatcollection/item/
---
## GeneralFormatCollection indexer

Belirtilen dizinde genel bir biçim alır.

```csharp
public GeneralFormat this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Genel formattaki indeks. |

### Geri dönüş değeri

Genel bir format.

## Örnekler

Alan sonuçlarının nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Biçim uygulanmadan bir sonuç görüntüleyen bir alan eklemek için bir belge oluşturucu kullanın.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Bir alanın sonucuna, alanın özelliklerini kullanarak bir format uygulayabiliriz.
// Aşağıda bir alanın sonucuna uygulayabileceğimiz üç tür format bulunmaktadır.
// 1 - Sayısal biçim:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Tarih/saat biçimi:
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

// Alanın sonucunu orijinal haline döndürmek için formatlarımızı kaldırabiliriz.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Ayrıca bakınız

* enum [GeneralFormat](../../generalformat/)
* class [GeneralFormatCollection](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
