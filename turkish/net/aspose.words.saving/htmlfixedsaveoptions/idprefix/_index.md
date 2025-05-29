---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: .NET için Aspose.Words
description: Belgelerinizdeki öğe kimliklerini özelleştirmek için HtmlFixedSaveOptions IdPrefix özelliğini keşfedin. Daha iyi çıktı için özelleştirilmiş öneklerle organizasyonu geliştirin!
type: docs
weight: 100
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

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

Oluşturulan tüm öğe kimliklerine eklenen bir önekin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
