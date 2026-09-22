---
title: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode yöntemi"
linktitle: "get_ImlRenderingMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode yöntemi. Ink (InkML) nesnelerinin C++'da nasıl işleneceğini belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


Mürekkep (InkML) nesnelerinin nasıl render edildiğini belirleyen bir değeri alır veya ayarlar.

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## Açıklamalar


Varsayılan değer [InkML](../../imlrenderingmode/)'dir.

Bu özellik, belge sabit sayfa biçimlerine dışa aktarıldığında kullanılır.

## Örnekler



Mürekkep nesnesinin nasıl render edileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// 'ImlRenderingMode.InkML' ayarı, mürekkep (InkML) nesnesinin geri dönüş şekline aldırmaz ve InkML'yi kendisi render eder.
// Render sonucu tatmin edici değilse,
// lütfen önceki sürümlere benzer bir sonuç elde etmek için 'ImlRenderingMode.Fallback' kullanın.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## Ayrıca Bakınız

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
