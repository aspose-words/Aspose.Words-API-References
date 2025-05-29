---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: .NET için Aspose.Words
description: Tasarımınızı geliştirmek için Border Shadow özelliğini keşfedin! Kenarlıklar için gölge efektlerini kontrol edin ve kullanıcı arayüzünüzü çarpıcı görsellerle yükseltin.
type: docs
weight: 60
url: /tr/net/aspose.words/border/shadow/
---
## Border.Shadow property

Sınırın gölgesi olup olmadığını belirten bir değer alır veya ayarlar.

```csharp
public bool Shadow { get; set; }
```

## Notlar

Microsoft Word'de, bir kenarlığın gölgeye sahip olması için, dört taraftaki kenarlıklar (sol, üst, sağ ve alt) aynı türde, genişlikte, renkte olmalı ve hepsinin Gölge özelliği şu şekilde ayarlanmalıdır:`doğru`.

## Örnekler

Gölgeli yeşil dalgalı sayfa kenarlığının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Ayrıca bakınız

* class [Border](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
