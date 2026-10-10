---
title: "Aspose::Words::Layout::ContinuousSectionRestart enum"
linktitle: "ContinuousSectionRestart"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::ContinuousSectionRestart enum. C++'ta sayfa numaralandırmasını yeniden başlatan sürekli bir bölümde sayfa numaraları hesaplanırken farklı davranışları temsil eder."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


Sayfa numaralandırmasını yeniden başlatan sürekli bir bölümde sayfa numaraları hesaplanırken farklı davranışları temsil eder.

```cpp
enum class ContinuousSectionRestart
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Her zaman | 0 | Sayfa numaralandırması, içerik akışına bakılmaksızın her zaman yeniden başlar. |
| FromNewPageOnly | 1 | Sayfa numaralandırması, bölümün başladığı sayfada bölümün önünde başka bir içerik olmadığında yalnızca yeniden başlar. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
