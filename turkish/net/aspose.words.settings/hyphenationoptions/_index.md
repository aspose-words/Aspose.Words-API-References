---
title: Class HyphenationOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Settings.HyphenationOptions sınıf. Belge tireleme seçeneklerini yapılandırmaya izin verir.
type: docs
weight: 5790
url: /tr/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Belge tireleme seçeneklerini yapılandırmaya izin verir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Tireleme ile Çalışmak](https://docs.aspose.com/words/net/working-with-hyphenation/) dokümantasyon makalesi.

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
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Belge için otomatik tirelemenin açık olup olmadığını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri:`YANLIŞ` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Kısa çizgilerle bitebilecek ardışık satırların maksimum sayısını alır veya ayarlar. Bu özelliğin varsayılan değeri 0. 'dir |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Tamamı büyük harflerle yazılan kelimelerin tireli olup olmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri:`doğru` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Sağ kenar boşluğundan, sözcükleri tirelemesini istemediğiniz noktanın 1/20'si kadar mesafeyi alır veya ayarlar. . Bu özellik için varsayılan değer 360'tır (0,25 inç). |

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


