---
title: "Aspose::Words::StyleCollection::ClearQuickStyleGallery yöntemi"
linktitle: "ClearQuickStyleGallery"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::StyleCollection::ClearQuickStyleGallery yöntemi. C++'ta Hızlı Stil Galerisi panelindeki tüm stilleri kaldırır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


Hızlı [Style](../../style/) Galeri panelindeki tüm stilleri kaldırır.

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## Örnekler



[Style](../../style/) Galeri panelinden stilleri nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
// Not: Stil kaldırma şu anda yalnızca DOCX formatında çalışır.
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(get_ArtifactsDir() + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## Ayrıca Bakınız

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
