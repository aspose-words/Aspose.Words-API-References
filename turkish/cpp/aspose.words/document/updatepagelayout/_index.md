---
title: "Aspose::Words::Document::UpdatePageLayout metodu"
linktitle: "UpdatePageLayout"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::UpdatePageLayout metodu. Belgenin sayfa düzenini C++'ta yeniden oluşturur."
type: docs
weight: 98000
url: /tr/cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


Belgenin sayfa düzenini yeniden oluşturur.

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## Açıklamalar


Bu metod belgeyi sayfalara biçimlendirir ve PAGE, PAGES, PAGEREF ve REF gibi sayfa numarasıyla ilgili alanları belgedeki günceller. Güncel sayfa düzeni bilgisi, belgenin sabit sayfa formatlarına doğru şekilde render edilmesi için gereklidir.

Bu metod, bir belgeyi ilk kez PDF, XPS, görüntüye dönüştürdüğünüzde veya yazdırdığınızda otomatik olarak çağrılır. Ancak, belgeyi render ettikten sonra değiştirir ve tekrar render etmeye çalışırsanız - Aspose.Words sayfa düzenini otomatik olarak güncellemez. Bu durumda, tekrar render etmeden önce [UpdatePageLayout](./) metodunu çağırmalısınız.

## Örnekler



Belge sayfa düzeninin ne zaman yeniden hesaplanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Bir belgeyi PDF'ye, bir görüntüye kaydetmek ya da ilk kez yazdırmak otomatik olarak
// belgenin sayfaları içinde düzeni önbelleğe alır.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Belgeyi bir şekilde değiştirin.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// Mevcut Aspose.Words sürümünde, belgeyi değiştirmek otomatik olarak yeniden oluşturmaz
// önbelleğe alınmış sayfa düzeni. Önbelleğe alınmış düzeni istersek
// güncel kalması için, manuel olarak güncellememiz gerekecek.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
