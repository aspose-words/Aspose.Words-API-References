---
title: ControlChar.Cr
second_title: Aspose.Words for .NET API Referansı
description: ControlChar alan. Satırbaşı karakteri x000d veya r. İle aynıParagraphBreak .
type: docs
weight: 50
url: /tr/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Satırbaşı karakteri: "\x000d" veya "\r". İle aynı[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

### Örnekler

Kontrol karakterlerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder ile metin içeren paragraflar ekleyin.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Belgeyi metin biçimine dönüştürmek, kontrol karakterlerinin ortaya çıktığını gösterir
// sayfa sonları gibi belgenin bazı yapısal öğelerini temsil eder.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Bir belgeyi string biçimine dönüştürürken,
// Trim metodu ile bazı kontrol karakterlerini atlayabiliriz.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [ControlChar](../)
* ad alanı [Aspose.Words](../../controlchar/)
* toplantı [Aspose.Words](../../../)


