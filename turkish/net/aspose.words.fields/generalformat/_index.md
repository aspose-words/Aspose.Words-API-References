---
title: GeneralFormat Enum
linktitle: GeneralFormat
articleTitle: GeneralFormat
second_title: .NET için Aspose.Words
description: Alanlar için sayısal metin biçimlendirmesini geliştiren, belgelerinizde açıklık ve kesinlik sağlayan Aspose.Words.Fields.GeneralFormat enum'unu keşfedin.
type: docs
weight: 3050
url: /tr/net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

Sayısal, metin veya herhangi bir alan sonucuna uygulanan genel bir biçimi belirtir. Bir alan, genel biçimlerin bir kombinasyonuna sahip olabilir.

```csharp
public enum GeneralFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Eksik genel bir formatı belirtmek için kullanılır. |
| Aiueo | `1` | Sayısal biçimlendirme. Sayısal bir sonucu geleneksel aiueo sırasına göre hiragana karakterleri kullanarak biçimlendirir. |
| UppercaseAlphabetic | `2` | Sayısal biçimlendirme. Sayısal sonucu büyük harfli alfabetik Latin karakterinin bir veya daha fazla örneği olarak biçimlendirir. |
| LowercaseAlphabetic | `3` | Sayısal biçimlendirme. Sayısal sonucu küçük harfli alfabetik Latin karakterinin bir veya daha fazla örneği olarak biçimlendirir. |
| Arabic | `4` | Sayısal biçimlendirme. Sayısal bir sonucu Arap temel rakamlarını kullanarak biçimlendirir. |
| ArabicAbjad | `5` | Sayısal biçimlendirme. Sayısal sonucu artan Abjad rakamları kullanarak biçimlendirir. |
| ArabicAlpha | `6` | Sayısal biçimlendirme. Sayısal bir sonucu Arap alfabesindeki karakterleri kullanarak biçimlendirir. |
| ArabicDash | `7` | Sayısal biçimlendirme. Sayısal bir sonucu, "-" öneki ve "-" son eki ile Arap asıl rakamları kullanarak biçimlendirir. |
| BahtText | `8` | Sayısal biçimlendirme. Sayısal bir sonucu Tay sayım sisteminde biçimlendirir. |
| CardText | `9` | Sayısal biçimlendirme. Ana metin (Bir, İki, Üç, ...). |
| ChineseNum1 | `10` | Sayısal biçimlendirme. Sayısal sonucu uygun sayma sisteminden artan sayılar kullanarak biçimlendirir. |
| ChineseNum2 | `11` | Sayısal biçimlendirme. Sayısal sonucu uygun yasal biçimden ardışık sayılar kullanarak biçimlendirir. |
| ChineseNum3 | `12` | Sayısal biçimlendirme. Sayısal sonucu, uygun sayma binlik sisteminden gelen ardışık sayıları kullanarak biçimlendirir. |
| Chosung | `13` | Sayısal biçimlendirme. Kore Chosung biçiminden ardışık sayılar kullanarak sayısal bir sonucu biçimlendirir. |
| CircleNum | `14` | Sayısal biçimlendirme. Sayısal sonucu, 1–20 aralığındaki sayılar için içindeki alfanümerik glif karakterini kullanarak, daire içine alınmış ondalık numaralandırma kullanarak biçimlendirir. |
| DBChar | `15` | Sayısal biçimlendirme. Sayısal sonucu çift baytlı Arapça numaralandırma kullanarak biçimlendirir. |
| DBNum1 | `16` | Sayısal biçimlendirme. Sıralı dijital ideogramları kullanarak, uygun karakteri kullanarak sayısal bir sonucu biçimlendirir. |
| DBNum2 | `17` | Sayısal biçimlendirme. Sayısal sonucu, uygun sayma sisteminden gelen ardışık sayıları kullanarak biçimlendirir. |
| DBNum3 | `18` | Sayısal biçimlendirme. Sayısal sonucu, uygun yasal sayım sisteminden gelen ardışık sayıları kullanarak biçimlendirir. |
| DBNum4 | `19` | Sayısal biçimlendirme. Uygun dijital sayma sisteminden gelen ardışık sayıları kullanarak sayısal bir sonucu biçimlendirir. |
| DollarText | `20` | Sayısal biçimlendirme. Dolar metni (Bir, İki, Üç, ... + VE 55/100). |
| Ganada | `21` | Sayısal biçimlendirme. Kore Ganada biçiminden ardışık sayılar kullanarak sayısal bir sonucu biçimlendirir. |
| GB1 | `22` | Sayısal biçimlendirme. Sayısal sonucu, ondalık numaralandırmayı ve ardından noktayı kullanarak biçimlendirir ve kapalı alfanümerik glif karakterini kullanır. |
| GB2 | `23` | Sayısal biçimlendirme. Sayısal sonucu parantez içinde ondalık numaralandırma kullanarak biçimlendirir, kapalı alfanümerik glif karakterini kullanarak. |
| GB3 | `24` | Sayısal biçimlendirme. Sayısal sonucu, daire içine alınmış ondalık numaralandırmayı kullanarak biçimlendirir ve içine alınmış alfanümerik glif karakterini kullanır. |
| GB4 | `25` | Sayısal biçimlendirme. Sayısal sonucu, daire içine alınmış ondalık numaralandırmayı kullanarak biçimlendirir ve içine alınmış alfanümerik glif karakterini kullanır. |
| Hebrew1 | `26` | Sayısal biçimlendirme. Sayısal bir sonucu İbranice rakamları kullanarak biçimlendirir. |
| Hebrew2 | `27` | Sayısal biçimlendirme. Sayısal bir sonucu İbrani alfabesini kullanarak biçimlendirir. |
| Hex | `28` | Sayısal biçimlendirme. Sayısal sonucu büyük harfli onaltılık basamaklar kullanarak biçimlendirir. |
| HindiArabic | `29` | Sayısal biçimlendirme. Sayısal bir sonucu Hintçe sayılar kullanarak biçimlendirir. |
| HindiCardText | `30` | Sayısal biçimlendirme. Sayısal sonucu, Hintçe sayma sisteminden gelen ardışık sayıları kullanarak biçimlendirir. |
| HindiLetter1 | `31` | Sayısal biçimlendirme. Sayısal bir sonucu Hintçe ünlülerini kullanarak biçimlendirir. |
| HindiLetter2 | `32` | Sayısal biçimlendirme. Sayısal bir sonucu Hintçe ünsüzlerini kullanarak biçimlendirir. |
| Iroha | `33` | Sayısal biçimlendirme. Sayısal bir sonucu Japonca iroha kullanarak biçimlendirir. |
| KanjiNum1 | `34` | Sayısal biçimlendirme. Uygun sayma sistemini kullanarak sayısal sonucu Japonca stilinde biçimlendirir. |
| KanjiNum2 | `35` | Sayısal biçimlendirme. Sayısal sonucu uygun sayma sistemini kullanarak biçimlendirir. |
| KanjiNum3 | `36` | Sayısal biçimlendirme. Sayısal sonucu uygun sayma sistemini kullanarak biçimlendirir. |
| Ordinal | `37` | Sayısal biçimlendirme. Sıralı (1., 2., 3., ...). |
| OrdText | `38` | Sayısal biçimlendirme. Sıralı metin (Birinci, İkinci, Üçüncü, ...). |
| UppercaseRoman | `39` | Sayısal biçimlendirme. Büyük harfli Roma (I, II, III, ...). |
| LowercaseRoman | `40` | Sayısal biçimlendirme. Küçük harfli Roma (i, ii, iii, ...). |
| SBChar | `41` | Sayısal biçimlendirme. Sayısal sonucu tek baytlık Arapça numaralandırma kullanarak biçimlendirir. |
| ThaiArabic | `42` | Sayısal biçimlendirme. Sayısal bir sonucu Tayca rakamları kullanarak biçimlendirir. |
| ThaiCardText | `43` | Sayısal biçimlendirme. Sayısal bir sonucu, Tay sayma sisteminden gelen ardışık sayıları kullanarak biçimlendirir. |
| ThaiLetter | `44` | Sayısal biçimlendirme. Sayısal bir sonucu Tayca harfleri kullanarak biçimlendirir. |
| VietCardText | `45` | Sayısal biçimlendirme. Sayısal bir sonucu Vietnamca rakamları kullanarak biçimlendirir. |
| Zodiac1 | `46` | Sayısal biçimlendirme. Sıralı sayısal geleneksel ideogramları kullanarak sayısal bir sonucu biçimlendirir. |
| Zodiac2 | `47` | Sayısal biçimlendirme. Sıralı zodyak ideogramlarını kullanarak sayısal bir sonucu biçimlendirir. |
| Zodiac3 | `48` | Sayısal biçimlendirme. Sıralı geleneksel zodyak ideogramlarını kullanarak sayısal bir sonucu biçimlendirir. |
| Caps | `49` | Metin biçimlendirme. Her kelimenin ilk harfini büyük harfe dönüştürür. |
| FirstCap | `50` | Metin biçimlendirme. İlk kelimenin ilk harfini büyük yapar. |
| Lower | `51` | Metin biçimlendirmesi. Tüm harfler küçük harftir. |
| Upper | `52` | Metin biçimlendirmesi. Tüm harfler büyük harftir. |
| CharFormat | `53` | Alan sonucu biçimlendirme. CHARFORMAT talimatı. |
| MergeFormat | `54` | Alan sonucu biçimlendirme. MERGEFORMAT talimatı. |
| MergeFormatInet | `55` | Alan sonucu biçimlendirme. MERGEFORMATINET talimatı. |

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
