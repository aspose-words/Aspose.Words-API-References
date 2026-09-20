---
title: "Aspose::Words::Drawing::Fill::get_TextureAlignment метод"
linktitle: "get_TextureAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Fill::get_TextureAlignment метод. Получает или задает выравнивание для заливки плиточной текстурой в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words.drawing/fill/get_texturealignment/
---
## Fill::get_TextureAlignment method


Получает или задает выравнивание для плиточной текстурной заливки.

```cpp
Aspose::Words::Drawing::TextureAlignment Aspose::Words::Drawing::Fill::get_TextureAlignment()
```


## Примеры



Показывает, как заполнить и замостить текстуру внутри фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// Применить выравнивание текстуры к заполнению фигуры.
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// Используйте параметр совместимости, чтобы определить фигуру с помощью DML, если вы хотите получить "TextureAlignment"
// свойство после сохранения документа.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## См. также

* Enum [TextureAlignment](../../texturealignment/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
