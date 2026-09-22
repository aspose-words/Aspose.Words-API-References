---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat yöntemi"
linktitle: "get_SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat yöntemi. Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği biçimi belirtir. C++'ta yalnızca Docling olabilir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/doclingsaveoptions/get_saveformat/
---
## DoclingSaveOptions::get_SaveFormat method


Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği biçimi belirtir. Yalnızca [Docling](../../../aspose.words/saveformat/) olabilir.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat() override
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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
