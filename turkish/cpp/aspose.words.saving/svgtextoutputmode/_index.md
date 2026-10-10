---
title: "Aspose::Words::Saving::SvgTextOutputMode enum"
linktitle: "SvgTextOutputMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SvgTextOutputMode enum. Bir belgedeki metnin SVG formatında C++ ile kaydedilirken nasıl render edileceğini belirtmeye olanak tanır."
type: docs
weight: 83000
url: /tr/cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


Bir belge içindeki metnin SVG formatında kaydedilirken nasıl render edileceğini belirtmeye olanak tanır.

```cpp
enum class SvgTextOutputMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| UseSvgFonts | 0 | Metni render etmek için SVG yazı tipleri kullanılır. Not: tüm tarayıcılar SVG yazı tiplerini desteklemez. |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) hedef makinede yüklü olduğunda metni render etmek için kullanılır. Not: belgede kullanılan bazı yazı tipleri hedef makinede mevcut değilse, belge farklı görünebilir. |
| UsePlacedGlyphs | 2 | Metin eğriler kullanılarak render edilir. Not: bu seçeneği kullanırsanız metin seçimi çalışmayacaktır. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
