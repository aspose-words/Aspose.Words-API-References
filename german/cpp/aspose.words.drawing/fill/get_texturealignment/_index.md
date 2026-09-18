---
title: "Aspose::Words::Drawing::Fill::get_TextureAlignment Methode"
linktitle: "get_TextureAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill::get_TextureAlignment Methode. Gibt die Ausrichtung für die Kacheltexturfüllung in C++ zurück oder setzt sie."
type: docs
weight: 20000
url: /de/cpp/aspose.words.drawing/fill/get_texturealignment/
---
## Fill::get_TextureAlignment method


Liest oder legt die Ausrichtung für Kacheltextur-Füllung fest.

```cpp
Aspose::Words::Drawing::TextureAlignment Aspose::Words::Drawing::Fill::get_TextureAlignment()
```


## Beispiele



Zeigt, wie die Textur innerhalb der Form gefüllt und gekachelt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// Textur-Ausrichtung auf die Formfüllung anwenden.
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// Verwenden Sie die Compliance-Option, um die Form mit DML zu definieren, wenn Sie "TextureAlignment" erhalten möchten.
// Eigenschaft nach dem Speichern des Dokuments.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## Siehe auch

* Enum [TextureAlignment](../../texturealignment/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
