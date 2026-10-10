---
title: "Aspose::Words::Drawing::TextureAlignment enum"
linktitle: "TextureAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextureAlignment enum. Gibt die Ausrichtung für die Kachelung der Texturfüllung in C++ an."
type: docs
weight: 42000
url: /de/cpp/aspose.words.drawing/texturealignment/
---
## TextureAlignment enum


Gibt die Ausrichtung für die Kachelung der Texturfüllung an.

```cpp
enum class TextureAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| TopLeft | 0 | Obere linke Texturausrichtung. |
| Oben | 1 | Obere Textur-Ausrichtung. |
| TopRight | 2 | Obere rechte Textur-Ausrichtung. |
| Links | 3 | Linke Textur-Ausrichtung. |
| Mitte | 4 | Zentrierte Textur-Ausrichtung. |
| Rechts | 5 | Rechte Textur-Ausrichtung. |
| BottomLeft | 6 | Untere linke Textur-Ausrichtung. |
| Unten | 7 | Untere Textur-Ausrichtung. |
| BottomRight | 8 | Untere rechte Textur-Ausrichtung. |
| Keine | 9 | Keine Textur-Ausrichtung. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
