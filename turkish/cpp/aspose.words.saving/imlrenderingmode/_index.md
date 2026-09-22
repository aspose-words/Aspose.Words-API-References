---
title: "Aspose::Words::Saving::ImlRenderingMode enum"
linktitle: "ImlRenderingMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImlRenderingMode enum. C++'ta mürekkep (InkML) nesnelerinin sabit sayfa formatlarına nasıl render edildiğini belirtir."
type: docs
weight: 66000
url: /tr/cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


Mürekkep (InkML) nesnelerinin sabit sayfa formatlarına nasıl işlendiğini belirtir.

```cpp
enum class ImlRenderingMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Yedek | 0 | Mürekkep (InkML) nesnesi için yedek şekil mevcutsa, Aspose.Words InkML yerine yedek şekli render eder. |
| InkML | 1 | Aspose.Words, mürekkep (InkML) nesnesinin geri dönüş şekline aldırmaz ve InkML'yi kendisi render eder. Bu varsayılan moddur. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
