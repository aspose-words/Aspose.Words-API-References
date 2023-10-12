---
title: Border.Shadow
second_title: Aspose.Words for .NET API Referansı
description: Border mülk. Kenarlığın gölgesi olup olmadığını belirten bir değer alır veya ayarlar.
type: docs
weight: 60
url: /tr/net/aspose.words/border/shadow/
---
## Border.Shadow property

Kenarlığın gölgesi olup olmadığını belirten bir değer alır veya ayarlar.

```csharp
public bool Shadow { get; set; }
```

### Notlar

Microsoft Word'de, bir kenarlığın gölgeye sahip olması için, dört kenardaki (sol, üst, sağ ve alt) kenarlıkların aynı türde, genişlikte ve renkte olması ve hepsinde Shadow özelliğinin olarak ayarlanması gerekir`doğru`.

### Örnekler

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
* ad alanı [Aspose.Words](../../border/)
* toplantı [Aspose.Words](../../../)


