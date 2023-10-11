---
title: PageSetup.Margins
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Ön ayarı döndürür veya ayarlarMargins sayfanın.
type: docs
weight: 260
url: /tr/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Ön ayarı döndürür veya ayarlar[`Margins`](../../margins/) sayfanın.

```csharp
public Margins Margins { get; set; }
```

### Örnekler

Belgenin sayfa düzeninin ne zaman yeniden hesaplanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi PDF'ye veya görüntüye kaydetmek veya ilk kez yazdırmak otomatik olarak
// sayfalarının içindeki belgenin düzenini önbelleğe al.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Belgeyi bir şekilde değiştirin.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // Aspose.Words'ün mevcut sürümünde belgeyi değiştirmek otomatik olarak yeniden oluşturmuyor
// önbelleğe alınan sayfa düzeni. Önbelleğe alınmış düzeni istiyorsak
// güncel kalmak için manuel olarak güncellememiz gerekecek.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Ayrıca bakınız

* enum [Margins](../../margins/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


