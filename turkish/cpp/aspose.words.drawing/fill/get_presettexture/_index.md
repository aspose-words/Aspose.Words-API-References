---
title: "Aspose::Words::Drawing::Fill::get_PresetTexture yöntemi"
linktitle: "get_PresetTexture"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::get_PresetTexture yöntemi. C++'da doldurma için bir PresetTexture alır."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.drawing/fill/get_presettexture/
---
## Fill::get_PresetTexture method


Doldurma için bir [PresetTexture](../../presettexture/) alır.

```cpp
Aspose::Words::Drawing::PresetTexture Aspose::Words::Drawing::Fill::get_PresetTexture()
```


## Örnekler



Şekil içinde dokuyu doldurma ve döşeme nasıl yapılır gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// Doku hizalamasını şekil doldurmasına uygula.
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// Şekli DML kullanarak tanımlamak ve "TextureAlignment" elde etmek istiyorsanız uyumluluk seçeneğini kullanın
// belge kaydedildikten sonra özellik.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## Ayrıca Bakınız

* Enum [PresetTexture](../../presettexture/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
