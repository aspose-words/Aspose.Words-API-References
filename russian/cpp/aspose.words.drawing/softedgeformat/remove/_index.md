---
title: "Метод Aspose::Words::Drawing::SoftEdgeFormat::Remove"
linktitle: "Remove"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::SoftEdgeFormat::Remove. Удаляет SoftEdgeFormat из родительского объекта в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat::Remove method


Удаляет [SoftEdgeFormat](../) из родительского объекта.

```cpp
void Aspose::Words::Drawing::SoftEdgeFormat::Remove()
```


## Примеры



Показывает, как работать с форматированием мягкого края.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Примените мягкий край к фигуре.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Загрузите документ с прямоугольной фигурой с мягким краем.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Проверьте радиус мягкого края.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Удалить мягкую кромку из фигуры.
softEdgeFormat->Remove();

// Проверьте радиус удалённой мягкой кромки.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```


Показывает, как установить ограничение разрешения изображения.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## См. также

* Class [SoftEdgeFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
