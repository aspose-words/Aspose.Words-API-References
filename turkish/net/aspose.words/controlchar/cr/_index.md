---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: .NET için Aspose.Words
description: Metin biçimlendirmeyi geliştiren satır başı karakteri (x000d veya r) olan ControlChar Cr'yi keşfedin. Benzersiz çözümlerimizle kodlamanızı basitleştirin!
type: docs
weight: 50
url: /tr/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Satır başı karakteri: "\x000d" veya "\r". Aynı[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

## Örnekler

Kontrol karakterlerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder ile metin içeren paragraflar ekleyin.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Belgenin metin biçimine dönüştürülmesi, kontrol karakterlerinin ortaya çıkmasını sağlar
// sayfa sonları gibi belgenin bazı yapısal öğelerini temsil eder.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Bir belgeyi dize biçimine dönüştürürken,
// Trim metoduyla bazı kontrol karakterlerini atlayabiliriz.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [ControlChar](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
