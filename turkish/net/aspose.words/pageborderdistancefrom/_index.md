---
title: PageBorderDistanceFrom Enum
linktitle: PageBorderDistanceFrom
articleTitle: PageBorderDistanceFrom
second_title: .NET için Aspose.Words
description: Kesin sayfa kenarlığı yerleşimi için Aspose.Words.PageBorderDistanceFrom numaralandırmasını keşfedin. En uygun kenar boşluğu konumlandırmasıyla belge biçimlendirmesini geliştirin.
type: docs
weight: 5080
url: /tr/net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

Sayfa kenarlığının sayfa kenar boşluğuna göre konumunu belirtir.

```csharp
public enum PageBorderDistanceFrom
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Text | `0` | Kenarlık konumu sayfa kenar boşluğundan ölçülür. |
| PageEdge | `1` | Kenarlık konumu sayfa kenarından ölçülür. |

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
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
