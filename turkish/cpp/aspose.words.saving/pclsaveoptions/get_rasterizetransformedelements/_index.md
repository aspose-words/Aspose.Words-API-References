---
title: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements yöntemi"
linktitle: "get_RasterizeTransformedElements"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements yöntemi. Karmaşık dönüştürülmüş öğelerin PCL belgesine kaydedilmeden önce rasterleştirilip rasterleştirilmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan değer C++'ta true'tir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


Karmaşık dönüştürülmüş öğelerin PCL belgesine kaydedilmeden önce rasterleştirilip rasterleştirilmeyeceğini belirleyen bir değeri alır veya ayarlar. Varsayılan **true**.

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
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

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
