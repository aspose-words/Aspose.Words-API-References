---
title: "Aspose::Words::Saving::PclSaveOptions::get_SaveFormat yöntemi"
linktitle: "get_SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PclSaveOptions::get_SaveFormat yöntemi. Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. C++'ta yalnızca Pcl olabilir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/pclsaveoptions/get_saveformat/
---
## PclSaveOptions::get_SaveFormat method


Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği formatı belirtir. Yalnızca [Pcl](../../../aspose.words/saveformat/) olabilir.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PclSaveOptions::get_SaveFormat() override
```


## Örnekler



Bir belgeyi PCL'ye kaydederken karmaşık öğelerin nasıl rasterleştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
