---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirmesi için belirli sayfalarda sayfa kenarlığı yazdırmayı kontrol etmek üzere Aspose.Words.PageBorderAppliesTo numaralandırmasını keşfedin.
type: docs
weight: 5070
url: /tr/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

Sayfa kenarlığının hangi sayfalara yazdırılacağını belirtir.

```csharp
public enum PageBorderAppliesTo
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| AllPages | `0` | Sayfa kenarlığı bölümün tüm sayfalarında gösterilir. |
| FirstPage | `1` | Sayfa kenarlığı yalnızca bölümün ilk sayfasında gösterilir. |
| OtherPages | `2` | Sayfa kenarlığı bölümün ilk sayfası hariç tüm sayfalarda gösterilir. |

## Örnekler

İlk sayfanın üst kısmına geniş mavi bantlı bir kenarlığın nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Ayrıca bakınız

* class [PageSetup](../pagesetup/)
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
