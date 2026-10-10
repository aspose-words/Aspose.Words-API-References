---
title: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder yöntemi"
linktitle: "get_ShowPageBorder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder yöntemi. Sayfanın dış çizgisine bir kenarlık eklenip eklenmeyeceğini kontrol eder. Varsayılan değer C++'ta true'tur."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions::get_ShowPageBorder method


Sayfanın dış çizgisine bir kenarlık eklenip eklenmeyeceğini kontrol eder. Varsayılan **true**'dur.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
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
