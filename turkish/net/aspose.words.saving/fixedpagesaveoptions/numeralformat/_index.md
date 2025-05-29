---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: .NET için Aspose.Words
description: Sayısal işlemeyi özelleştirmek için FixedPageSaveOptions NumeralFormat özelliğini keşfedin. Gelişmiş belge sunumu için Avrupa rakamlarına kolayca geçin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Alır veya ayarlar[`NumeralFormat`](../../numeralformat/) rakamların işlenmesi için kullanılır. Varsayılan olarak Avrupa rakamları kullanılır.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## Notlar

Bu özelliğin değeri değiştirilirse ve sayfa düzeni zaten oluşturulmuşsa [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) herhangi bir değişikliği güncellemek için otomatik olarak çağrılır.

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

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
