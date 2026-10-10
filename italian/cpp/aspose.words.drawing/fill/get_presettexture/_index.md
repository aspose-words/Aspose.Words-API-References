---
title: "metodo Aspose::Words::Drawing::Fill::get_PresetTexture"
linktitle: "get_PresetTexture"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Fill::get_PresetTexture. Ottiene un PresetTexture per il riempimento in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.drawing/fill/get_presettexture/
---
## Fill::get_PresetTexture method


Ottiene un [PresetTexture](../../presettexture/) per il riempimento.

```cpp
Aspose::Words::Drawing::PresetTexture Aspose::Words::Drawing::Fill::get_PresetTexture()
```


## Esempi



Mostra come riempire e ripetere la texture all'interno della forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// Applica l'allineamento della texture al riempimento della forma.
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// Usa l'opzione di conformità per definire la forma usando DML se desideri ottenere "TextureAlignment"
// proprietà dopo il salvataggio del documento.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## Vedi anche

* Enum [PresetTexture](../../presettexture/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
