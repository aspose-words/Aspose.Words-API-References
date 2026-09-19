---
title: "metodo Aspose::Words::Drawing::Fill::get_TextureAlignment"
linktitle: "get_TextureAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Drawing::Fill::get_TextureAlignment. Ottiene o imposta l'allineamento per il riempimento a trama di texture in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.drawing/fill/get_texturealignment/
---
## Fill::get_TextureAlignment method


Ottiene o imposta l'allineamento per il riempimento a piastrelle di texture.

```cpp
Aspose::Words::Drawing::TextureAlignment Aspose::Words::Drawing::Fill::get_TextureAlignment()
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

* Enum [TextureAlignment](../../texturealignment/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
