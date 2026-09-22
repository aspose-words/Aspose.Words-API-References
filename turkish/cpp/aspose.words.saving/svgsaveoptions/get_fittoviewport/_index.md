---
title: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort yöntemi"
linktitle: "get_FitToViewPort"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort yöntemi. Çıktı SVG'nin kullanılabilir görünüm alanını (tarayıcı penceresi veya kapsayıcı) doldurup doldurmayacağını belirtir. True olarak ayarlandığında, çıktı SVG'nin genişliği ve yüksekliği %100 olarak ayarlanır. Varsayılan değer C++'ta false'tur."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/svgsaveoptions/get_fittoviewport/
---
## SvgSaveOptions::get_FitToViewPort method


Çıktı SVG'sinin kullanılabilir görünüm alanını (tarayıcı penceresini veya kapsayıcıyı) doldurup doldurmayacağını belirtir. **true** olarak ayarlandığında çıktı SVG'nin genişliği ve yüksekliği %100 olarak ayarlanır. Varsayılan değer **false**'dur.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort() const
```


## Örnekler



.docx belgesini .svg'ye dönüştürürken görüntü özelliklerini taklit etmenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Sayfa kenarlıkları veya seçilebilir metin olmadan kaydetmek için SvgSaveOptions nesnesini yapılandırın.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## Ayrıca Bakınız

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
