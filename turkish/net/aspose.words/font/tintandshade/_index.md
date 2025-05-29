---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: .NET için Aspose.Words
description: Renkleri kolayca ayarlamak için Font TintAndShade özelliğini keşfedin! Canlı tasarımlar için gölgeleri açın veya koyulaştırın. Projelerinizi zahmetsizce geliştirin!
type: docs
weight: 530
url: /tr/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Bir rengi açan veya koyulaştıran bir double değeri alır veya ayarlar.

```csharp
public double TintAndShade { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Bu özelliği -1'den küçük veya 1'den büyük bir değere ayarlarsanız fırlatın. |
| InvalidOperationException | Bu özelliği ayarlarsanız atın[`Font`](../) tema dışı renklere sahip nesne. |

## Notlar

Bu özellik için izin verilen değerler -1 (en koyu) ile 1 (en açık) arasında değişmektedir.

Sıfır (0) nötrdür.

## Örnekler

Temalı stilin nasıl oluşturulacağını ve kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Tema yazı tipi özellikleriyle biraz stil yaratın.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
