---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: .NET için Aspose.Words
description: Belgeleriniz için tireleme ayarlarını zahmetsizce özelleştirmek ve metin sunumunu geliştirmek için Aspose.Words.Settings.HyphenationOptions sınıfını keşfedin.
type: docs
weight: 6620
url: /tr/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Belge tireleme seçeneklerini yapılandırmaya izin verir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Tireleme ile Çalışma](https://docs.aspose.com/words/net/working-with-hyphenation/) belgeleme makalesi.

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
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Belge için otomatik tirelemenin açık olup olmadığını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Tire ile bitebilecek ardışık satırların maksimum sayısını alır veya ayarlar. Bu özelliğin varsayılan değeri 0'dır. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Tümü büyük harflerle yazılmış kelimelerin tireli olup olmadığını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer`doğru` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Kelimeleri tirelemek istemediğiniz sağ kenar boşluğundan 1/20'lik bir noktadan uzaklığı alır veya ayarlar. Bu özellik için varsayılan değer 360'tır (0,25 inç). |

## Örnekler

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
