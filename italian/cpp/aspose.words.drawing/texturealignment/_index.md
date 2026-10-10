---
title: "Aspose::Words::Drawing::TextureAlignment enum"
linktitle: "TextureAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextureAlignment enum. Specifica l'allineamento per la disposizione a tasselli del riempimento texture in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words.drawing/texturealignment/
---
## TextureAlignment enum


Specifica l'allineamento per la tessellatura del riempimento texture.

```cpp
enum class TextureAlignment
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| TopLeft | 0 | Allineamento della texture in alto a sinistra. |
| Superiore | 1 | Allineamento della texture in alto. |
| TopRight | 2 | Allineamento della texture in alto a destra. |
| Sinistra | 3 | Allineamento della texture a sinistra. |
| Centro | 4 | Allineamento della texture al centro. |
| Destra | 5 | Allineamento della texture a destra. |
| BottomLeft | 6 | Allineamento della texture in basso a sinistra. |
| Inferiore | 7 | Allineamento della texture in basso. |
| BottomRight | 8 | Allineamento della texture in basso a destra. |
| None | 9 | Nessun allineamento della texture. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
