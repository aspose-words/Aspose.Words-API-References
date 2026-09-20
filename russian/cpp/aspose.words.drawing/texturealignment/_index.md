---
title: "Aspose::Words::Drawing::TextureAlignment перечисление"
linktitle: "TextureAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::TextureAlignment перечисление. Указывает выравнивание для черепицы заполнения текстурой в C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words.drawing/texturealignment/
---
## TextureAlignment enum


Указывает выравнивание для чередования текстурной заливки.

```cpp
enum class TextureAlignment
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| TopLeft | 0 | Выравнивание текстуры в верхнем левом углу. |
| Верх | 1 | Выравнивание текстуры сверху. |
| TopRight | 2 | Выравнивание текстуры в верхнем правом углу. |
| Слева | 3 | Выравнивание текстуры слева. |
| По центру | 4 | Выравнивание текстуры по центру. |
| Справа | 5 | Выравнивание текстуры справа. |
| BottomLeft | 6 | Выравнивание текстуры в нижнем левом углу. |
| Низ | 7 | Выравнивание текстуры снизу. |
| BottomRight | 8 | Выравнивание текстуры в нижнем правом углу. |
| None | 9 | Нет выравнивания текстуры. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
