---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: .NET için Aspose.Words
description: Daha iyi organizasyon ve netlik için çıktı belgenizdeki öğe kimliklerini özelleştiren SvgSaveOptions IdPrefix özelliğini keşfedin. SVG dosyalarınızı bugün geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

Çıktı belgesindeki tüm oluşturulan öğe kimliklerine eklenen bir önek belirtir. Varsayılan değer null'dır ve hiçbir önek eklenmez.

```csharp
public string IdPrefix { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | Değer yukarıda belirtilen şartları karşılamıyor. |

## Notlar

Önek belirtilirse, yalnızca harf, rakam, alt çizgi ve tire içerebilir, ve bir harfle başlamalıdır.

## Örnekler

Oluşturulan tüm öğe kimliklerine (svg) ön ek eklenmesinin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### Ayrıca bakınız

* class [SvgSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
