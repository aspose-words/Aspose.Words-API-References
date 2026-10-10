---
title: "Aspose::Words::ImportFormatOptions::get_ResolveThemeColors metodu"
linktitle: "get_ResolveThemeColors"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions::get_ResolveThemeColors yöntemi. Şekillerin tema renklerini zorunlu olarak çözümleyip çözümlemeyeceğini belirten bir boolean değerini alır veya ayarlar. Varsayılan değer C++'da false'tur."
type: docs
weight: 8500
url: /tr/cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


Şekillerin tema renklerini zorla çözümleyeceğini belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## Açıklamalar


Lütfen bu seçeneğin yalnızca [KeepSourceFormatting](../../importformatmode/) modunda geçerli olduğunu unutmayın.

Normalde, Aspose.Words, stilleri içe aktarırken biçimlendirme özniteliklerini doğrudan özniteliklere genişletmeden korunabiliyorsa kaynak tema renklerini çözümlemez. Ancak bu durumda içe aktarılan şekillerin gerçek renkleri, orijinal belgede sahip oldukları renklerden farklı olabilir. Bunun nedeni kaynak ve hedef belgelerdeki farklı tema renkleridir. Bu seçeneği **true** olarak ayarlamak, kaynak şekil tema renklerinin çözülmesini zorlar ve böylece şekillerin kaynak belgede sahip oldukları gerçek rengi korur.

## Örnekler



Şekillerin kaynak tema renklerini çözümlerek bir düğümün nasıl içe aktarılacağını gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Birincil altbilgiye gidin ve tema renklerini kullanan bir şekil ekleyin.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Tema renkleri çözümlenmiş şekilde kaynak altbilgiyi hedef belgeye aktarın,
// böylece şekil, kaynak belgeden gerçek rengini korur.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Ayrıca Bakınız

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
