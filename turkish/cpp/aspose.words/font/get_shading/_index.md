---
title: "Aspose::Words::Font::get_Shading yöntemi"
linktitle: "get_Shading"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Shading yöntemi. Yazı tipinin gölgelendirme biçimlendirmesine referans veren bir Shading nesnesi döndürür C++'ta."
type: docs
weight: 34000
url: /tr/cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


Yazı tipi için gölgelendirme biçimlendirmesine referans veren bir [Shading](../../shading/) nesnesi döndürür.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## Örnekler



Bir belge oluşturucu tarafından oluşturulan metne gölgelendirme uygulamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// Beyaz yazı tipi rengimizle oluşturulan metni görünür kılmanın bir yolu
// arka plan gölgelendirme etkisi uygulamaktır.
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## Ayrıca Bakınız

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
