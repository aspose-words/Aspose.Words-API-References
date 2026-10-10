---
title: "Aspose::Words::Margins enum"
linktitle: "Margins"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Margins enum. C++'de önceden tanımlı kenar boşluklarını belirtir."
type: docs
weight: 99000
url: /tr/cpp/aspose.words/margins/
---
## Margins enum


Önceden ayarlanmış kenar boşluklarını belirtir.

```cpp
enum class Margins
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Normal | 0 | Normal kenar boşlukları. |
| Narrow | 1 | Dar kenar boşlukları. |
| Moderate | 2 | Orta kenar boşlukları. |
| Wide | 3 | Geniş kenar boşlukları. |
| Mirrored | 4 | Aynalı kenar boşlukları. |
| Özel | 5 | Custom margins. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
