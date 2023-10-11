---
title: Enum NumeralFormat
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.NumeralFormat Sıralama. Sabit sayfa formatlarında oluşturulurken sayıları temsil etmek için kullanılan sembol setini belirtir.
type: docs
weight: 5310
url: /tr/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Sabit sayfa formatlarında oluşturulurken sayıları temsil etmek için kullanılan sembol setini belirtir.

```csharp
public enum NumeralFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| European | `0` | Avrupa rakamları: 0123456789. |
| ArabicIndic | `1` | Arapçada kullanılan rakamlar: ٠١٢٣٤٥٦٧٨٩. Unicode aralığı U+0660 - u+0669. |
| EasternArabicIndic | `2` | Farsça ve Urduca'da kullanılan rakamlar: ۰۱۲۳۴۵۶۷۸۹. Unicode aralığı U+06F0 - u+06F9. |
| Context | `3` | Sembol setine bağlamdan (yerel ayar ve RTL özelliği) karar verilir. |
| System | `4` | BU SEÇENEK DESTEKLENMEMEKTEDİR. Sembol setine bölgesel ayarlardan karar verilir. |

### Örnekler

PDF'ye kaydederken kullanılan sayı biçiminin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// "NumeralFormat" özelliğini "NumeralFormat.ArabicIndic" olarak ayarlayın
// sayı olarak U+0660 ila U+0669 aralığındaki glifleri kullanın.
// "NumeralFormat" özelliğini "NumeralFormat.Context" olarak ayarlayın
// Hangi sayıda glifin kullanılacağını belirlemek için yerel ayarı arayın.
// "NumeralFormat" özelliğini "NumeralFormat.EasternArabicIndic" olarak ayarlayın
// sayı olarak U+06F0 ila U+06F9 aralığındaki glifleri kullanın.
// Avrupa rakamlarını kullanmak için "NumeralFormat" özelliğini "NumeralFormat.European" olarak ayarlayın.
// Sembol setini bölgesel ayarlardan belirlemek için "NumeralFormat" özelliğini "NumeralFormat.System" olarak ayarlayın.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


