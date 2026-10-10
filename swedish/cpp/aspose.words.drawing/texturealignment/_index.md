---
title: "Aspose::Words::Drawing::TextureAlignment enum"
linktitle: "TextureAlignment"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::TextureAlignment enum. Anger justeringen för kakelning av texturfyllning i C++."
type: docs
weight: 42000
url: /sv/cpp/aspose.words.drawing/texturealignment/
---
## TextureAlignment enum


Anger justeringen för mosaikfyllning av texturen.

```cpp
enum class TextureAlignment
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| TopLeft | 0 | Justering av textur uppe till vänster. |
| Top | 1 | Justering av textur uppe. |
| TopRight | 2 | Övre högra texturjustering. |
| Vänster | 3 | Vänster texturjustering. |
| Centrerad | 4 | Centrerad texturjustering. |
| Höger | 5 | Höger texturjustering. |
| BottomLeft | 6 | Nedre vänstra texturjustering. |
| Bottom | 7 | Nedre texturjustering. |
| BottomRight | 8 | Nedre högra texturjustering. |
| None | 9 | Ingen texturjustering. |


## Exempel



Visar hur man fyller och lägger texturen i formen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// Applicera texturjustering på formens fyllning.
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// Använd efterlevnadsalternativet för att definiera formen med DML om du vill få "TextureAlignment"
// egenskap efter att dokumentet sparas.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
