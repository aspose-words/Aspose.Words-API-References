---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: .NET için Aspose.Words
description: Sayfanızın Kenar Boşluklarını PageSetup özelliğiyle zahmetsizce ayarlayın. En iyi düzen ve sunum için ayarları özelleştirin. Belgenizin görünümünü geliştirin!
type: docs
weight: 260
url: /tr/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Ön ayarı döndürür veya ayarlar[`Margins`](../../margins/) sayfanın.

```csharp
public Margins Margins { get; set; }
```

## Örnekler

Belgenin sayfa düzeninin ne zaman yeniden hesaplanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi PDF'e, görüntüye kaydetmek veya ilk kez yazdırmak otomatik olarak
// Belgenin düzenini sayfalarının içinde önbelleğe al.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Belgeyi bir şekilde değiştirin.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Aspose.Words'ün geçerli sürümünde, belgeyi değiştirmek otomatik olarak yeniden oluşturmaz
// önbelleğe alınmış sayfa düzeni. Önbelleğe alınmış düzeni istiyorsak
// Güncel kalmak için manuel olarak güncellememiz gerekecek.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Ayrıca bakınız

* enum [Margins](../../margins/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
