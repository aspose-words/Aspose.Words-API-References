---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: .NET için Aspose.Words
description: Belgenizin yapısını UpdatePageLayout yöntemiyle yenileyin; gelişmiş okunabilirlik ve sunum için cilalı ve düzenli bir düzen sağlayın.
type: docs
weight: 830
url: /tr/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Belgenin sayfa düzenini yeniden oluşturur.

```csharp
public void UpdatePageLayout()
```

## Notlar

Bu yöntem bir belgeyi sayfalara biçimlendirir ve belgedeki sayfa numarasıyla ilgili alanları (örneğin PAGE, PAGES, PAGEREF ve REF) günceller. Güncel sayfa düzeni bilgileri, document 'nin sabit sayfa biçimlerine doğru bir şekilde işlenmesi için gereklidir.

Bu yöntem, bir belgeyi ilk kez PDF, XPS, görüntüye dönüştürdüğünüzde veya yazdırdığınızda otomatik olarak çağrılır. Ancak, belgeyi işledikten sonra değiştirirseniz ve sonra tekrar işlemeye çalışırsanız - Aspose.Words sayfa düzenini otomatik olarak güncellemez. Bu durumda şunu çağırmalısınız`UpdatePageLayout` before tekrar işleniyor.

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

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
