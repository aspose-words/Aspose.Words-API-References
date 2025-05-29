---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: .NET için Aspose.Words
description: HtmlLoadOptions SupportVml özelliğinin, gelişmiş grafik kalitesi için VML görüntü desteğini etkinleştirerek web deneyiminizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

VML görüntülerinin desteklenip desteklenmeyeceğini belirten bir değer alır veya ayarlar.

```csharp
public bool SupportVml { get; set; }
```

## Örnekler

Bir HTML belgesi yüklenirken koşullu yorumların nasıl destekleneceğini gösterir.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Değer doğruysa, yüklenen belgeyi ayrıştırırken VML kodunu dikkate alırız.
loadOptions.SupportVml = supportVml;

// Bu belge "<!--[if gte vml 1]>" etiketleri arasında bir JPEG görüntüsü içeriyor,
// ve "<![if !vml]>" etiketleri arasında farklı bir PNG resmi.
// "SupportVml" bayrağını "true" olarak ayarlarsak, Aspose.Words JPEG'i yükleyecektir.
// Bu bayrağı "false" olarak ayarlarsak, Aspose.Words yalnızca PNG'yi yükleyecektir.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Ayrıca bakınız

* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
