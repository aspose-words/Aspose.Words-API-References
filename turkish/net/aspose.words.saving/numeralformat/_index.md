---
title: NumeralFormat Enum
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: .NET için Aspose.Words
description: Sabit sayfa formatlarında en iyi sayı gösterimi için Aspose.Words.Saving.NumeralFormat enum'unu keşfedin. Belgenizin işlenmesini bugün geliştirin!
type: docs
weight: 6090
url: /tr/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Sabit sayfa biçimlerine dönüştürme sırasında sayıları temsil etmek için kullanılan sembol kümesini belirtir.

```csharp
public enum NumeralFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| European | `0` | Avrupa rakamları: 0123456789. |
| ArabicIndic | `1` | Arapçada kullanılan rakamlar: ٠١٢٣٤٥٦٧٨٩. Unicode aralığı U+0660 - u+0669. |
| EasternArabicIndic | `2` | Farsça ve Urducada kullanılan rakamlar: ۰۱۲۳۴۵۶۷۸۹. Unicode aralığı U+06F0 - u+06F9. |
| Context | `3` | Sembol seti, context(locale ve RTL özelliği) tarafından belirlenir. |
| System | `4` | BU SEÇENEK DESTEKLENMİYOR. Sembol seti bölgesel ayarlardan belirlenir. |

## Örnekler

PDF'e kaydederken kullanılan sayısal formatın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// "NumeralFormat" özelliğini "NumeralFormat.ArabicIndic" olarak ayarlayın
// U+0660 ile U+0669 aralığındaki glifleri sayı olarak kullan.
// "NumeralFormat" özelliğini "NumeralFormat.Context" olarak ayarlayın
// kaç adet glif kullanılacağını belirlemek için yerel ayarlara bakın.
// "NumeralFormat" özelliğini "NumeralFormat.EasternArabicIndic" olarak ayarlayın
// U+06F0 ile U+06F9 aralığındaki glifleri sayı olarak kullan.
// Avrupa rakamlarını kullanmak için "NumeralFormat" özelliğini "NumeralFormat.European" olarak ayarlayın.
// Bölgesel ayarlardan sembol kümesini belirlemek için "NumeralFormat" özelliğini "NumeralFormat.System" olarak ayarlayın.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
