---
title: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart yöntemi"
linktitle: "get_ContinuousSectionPageNumberingRestart"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart yöntemi. C++'da bir sürekli bölüm sayfa numaralandırmasını yeniden başlattığında sayfa numaralarını hesaplama davranış modunu alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


Sürekli bir bölüm sayfa numaralandırmasını yeniden başlattığında sayfa numaralarını hesaplama davranış modunu alır veya ayarlar.

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


## Örnekler



Sürekli bir bölümde sayfa numaralandırmasını nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// Varsayılan olarak Aspose.Words davranışı Microsoft Word 2019 ile eşleşir.
// Eski Aspose.Words davranışı, tekrarlayan Microsoft Word 2016'ya ihtiyacınız varsa, 'ContinuousSectionRestart.FromNewPageOnly' kullanın.
// Sayfa numaralandırması, bölümün başladığı sayfada bölümün önünde başka bir içerik olmadığında yalnızca yeniden başlar,
// bu yüzden numaralandırma ikinci sayfadan itibaren 2'ye sıfırlanır.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## Ayrıca Bakınız

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
