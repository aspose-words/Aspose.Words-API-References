---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes yöntemi"
linktitle: "get_RenderNonImageShapes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes yöntemi. C++'ta görüntü olmayan şekillerin render edilip çıktı Docling JSON belgesine yazılıp yazılmayacağını gösteren bir değeri alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


Görüntü olmayan şekillerin işlenip çıktı Docling JSON belgesine yazılıp yazılmayacağını gösteren bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
```


## Örnekler



Bir belgeyi Docling JSON biçimine nasıl kaydedeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// Görüntü olmayan şekilleri işlemek ve çıktıya dahil etmek için true olarak ayarlayın.
// Görüntü olmayan şekilleri çıktıda dışlamak için false (varsayılan) olarak ayarlayın.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## Ayrıca Bakınız

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
