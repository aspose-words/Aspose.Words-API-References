---
title: UpdatePageLayout
second_title: Aspose.Words for .NET API Referansı
description: Belgenin sayfa düzenini yeniden oluşturur.
type: docs
weight: 750
url: /tr/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Belgenin sayfa düzenini yeniden oluşturur.

```csharp
public void UpdatePageLayout()
```

### Notlar

Bu yöntem, bir belgeyi sayfalar halinde biçimlendirir ve belgedeki SAYFA, SAYFALAR, PAGEREF ve REF gibi gibi sayfa numarasıyla ilgili alanları günceller. Document belgesinin sabit sayfa biçimlerine doğru şekilde oluşturulması için güncel sayfa düzeni bilgileri gereklidir.

Bu yöntem, bir belgeyi ilk kez PDF, XPS, görüntüye dönüştürdüğünüzde veya yazdırdığınızda otomatik olarak çağrılır. Ancak, belgeyi oluşturduktan sonra değiştirir ve ardından yeniden oluşturmayı denerseniz - Aspose.Words sayfa düzenini otomatik olarak güncellemeyecektir . Bu durumda aramanız gerekir`UpdatePageLayout` Before yeniden oluşturuluyor.

### Örnekler

Belgenin sayfa düzeninin ne zaman yeniden hesaplanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi PDF'ye, bir görüntüye kaydetmek veya ilk kez yazdırmak otomatik olarak
// belgenin düzenini sayfalarında önbelleğe al.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Belgeyi bir şekilde değiştirin.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;

 // Aspose.Words'ün mevcut sürümünde, belgeyi değiştirmek otomatik olarak yeniden oluşturmaz
// önbelleğe alınmış sayfa düzeni. Önbelleğe alınmış düzen için istersek
// güncel kalmak için manuel olarak güncellememiz gerekecek.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Ayrıca bakınız

* class [Document](../../document)
* ad alanı [Aspose.Words](../../document)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
