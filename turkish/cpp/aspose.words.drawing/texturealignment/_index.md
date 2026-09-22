---
title: "Aspose::Words::Drawing::TextureAlignment enum"
linktitle: "TextureAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::TextureAlignment enum. Doku doldurmanın döşenmesi için hizalamayı C++'da belirtir."
type: docs
weight: 42000
url: /tr/cpp/aspose.words.drawing/texturealignment/
---
## TextureAlignment enum


Doku doldurmanın döşenmesi için hizalamayı belirtir.

```cpp
enum class TextureAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| ÜstSol | 0 | Üst sol doku hizalaması. |
| Üst | 1 | Üst doku hizalaması. |
| ÜstSağ | 2 | Üst sağ doku hizalaması. |
| Sol | 3 | Sol doku hizalaması. |
| Orta | 4 | Orta doku hizalaması. |
| Sağ | 5 | Sağ doku hizalaması. |
| AltSol | 6 | Alt sol doku hizalaması. |
| Alt | 7 | Alt doku hizalaması. |
| AltSağ | 8 | Alt sağ doku hizalaması. |
| None | 9 | Hiç doku hizalaması. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
