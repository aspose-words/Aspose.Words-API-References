---
title: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode metodu"
linktitle: "get_TextOutputMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode metodu. C++'ta SVG içinde metnin nasıl render edileceğini belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions::get_TextOutputMode method


SVG'de metnin nasıl render edileceğini belirleyen bir değeri alır veya ayarlar.

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```

## Açıklamalar


Bu özelliği, bir belge içindeki metnin SVG formatında kaydedilirken nasıl render edileceği modunu almak veya ayarlamak için kullanın.

Varsayılan değer [UseTargetMachineFonts](../../svgtextoutputmode/)'dır.

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

* Enum [SvgTextOutputMode](../../svgtextoutputmode/)
* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
