---
title: "Aspose::Words::Drawing::ShadowFormat::get_Transparency metodu"
linktitle: "get_Transparency"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShadowFormat::get_Transparency metodu. Gölge etkisi için şeffaflık derecesini 0.0 (opak) ile 1.0 (temiz) arasında bir değer olarak alır veya ayarlar. Varsayılan değer C++'ta 0.0'dır."
type: docs
weight: 2750
url: /tr/cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


Gölge etkisi için şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır veya ayarlar. Varsayılan değer 0.0'dır.

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## Örnekler



Şeffaflık ile bir rengi nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## Ayrıca Bakınız

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
