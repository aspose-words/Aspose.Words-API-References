---
title: "Aspose::Words::PageSetup::get_Margins metodu"
linktitle: "get_Margins"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_Margins metodu. Sayfanın önceden ayarlanmış Kenar Boşluklarını C++'ta döndürür veya ayarlar."
type: docs
weight: 28000
url: /tr/cpp/aspose.words/pagesetup/get_margins/
---
## PageSetup::get_Margins method


Sayfanın önceden ayarlanmış [Margins](../../margins/) değerlerini döndürür veya ayarlar.

```cpp
Aspose::Words::Margins Aspose::Words::PageSetup::get_Margins()
```


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

* Enum [Margins](../../margins/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
