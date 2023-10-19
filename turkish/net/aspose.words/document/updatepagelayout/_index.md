---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words for .NET
description: Document UpdatePageLayout yöntem. Belgenin sayfa düzenini yeniden oluşturur C#'da.
type: docs
weight: 770
url: /tr/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Belgenin sayfa düzenini yeniden oluşturur.

```csharp
public void UpdatePageLayout()
```

## Notlar

Bu yöntem, bir belgeyi sayfalar halinde biçimlendirir ve belgedeki PAGE, PAGES, PAGEREF ve REF gibi gibi sayfa numarasıyla ilgili alanları günceller. document dosyasının sabit sayfa formatlarına doğru şekilde işlenmesi için güncel sayfa düzeni bilgileri gereklidir.

Bu yöntem, bir belgeyi ilk kez PDF'ye, XPS'ye, görüntüye dönüştürdüğünüzde veya yazdırdığınızda otomatik olarak çağrılır. Ancak, belgeyi oluşturduktan sonra değiştirirseniz ve tekrar oluşturmaya çalışırsanız - Aspose.Words sayfa düzenini otomatik olarak güncellemez. Bu durumda aramalısınız`UpdatePageLayout` before yeniden oluşturuluyor.

## Örnekler

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

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
