---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words for .NET
description: FixedPageSaveOptions NumeralFormat mülk. Alır veya ayarlarNumeralFormat rakamların oluşturulması için kullanılır. Avrupa rakamları varsayılan olarak kullanılır C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Alır veya ayarlar[`NumeralFormat`](../../numeralformat/) rakamların oluşturulması için kullanılır. Avrupa rakamları varsayılan olarak kullanılır.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## Notlar

Bu özelliğin değeri değiştirilmişse ve sayfa düzeni zaten oluşturulmuşsa Then [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) herhangi bir değişikliği güncellemek için otomatik olarak çağrılır.

## Örnekler

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

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
