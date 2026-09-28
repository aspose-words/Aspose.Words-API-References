---
title: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer метод"
linktitle: "GetShapeRenderer"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer метод. Создает и возвращает объект, который можно использовать для отрисовки этой формы в изображение в C++."
type: docs
weight: 58000
url: /ru/cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


Создаёт и возвращает объект, который можно использовать для отрисовки этой фигуры в изображение.

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

Объект рендерера для этой формы.
## Примечания


Этот метод просто вызывает конструктор [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) и передает этот объект в качестве параметра.

## Примеры



Показывает, как использовать рендерер формы для экспорта форм в файлы в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// В документе 7 форм, включая одну групповую форму с 2 дочерними формами.
// Мы отрендерим каждую форму в файл изображения в локальной файловой системе
// игнорируя групповые фигуры, так как они не имеют внешнего вида.
// Это создаст 6 файлов изображений.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## См. также

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
