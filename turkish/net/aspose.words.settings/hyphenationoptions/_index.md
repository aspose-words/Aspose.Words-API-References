---
title: Class HyphenationOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Settings.HyphenationOptions sınıf. Belge tireleme seçeneklerini yapılandırmaya izin verir.
type: docs
weight: 5500
url: /tr/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Belge tireleme seçeneklerini yapılandırmaya izin verir.

```csharp
public class HyphenationOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Belge için otomatik tirelemenin açık olup olmadığını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer **yanlış** . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Kısa çizgi ile bitebilecek maksimum ardışık satır sayısını alır veya ayarlar. Bu özellik için varsayılan değer 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Tamamı büyük harflerle yazılan sözcüklerin tireli olup olmadığını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer **doğru** . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Kelimeleri tirelemek için istemediğiniz sağ kenar boşluğundan bir noktanın 1/20'si olarak mesafeyi alır veya ayarlar. Bu özellik için varsayılan değer 360'tır (0,25 inç). |

### Örnekler

Otomatik tirelemenin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)


