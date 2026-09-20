---
title: "Aspose::Words::Drawing::Shape::get_HasImage метод"
linktitle: "get_HasImage"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Shape::get_HasImage method. Возвращает true если у фигуры есть байты изображения или она ссылается на изображение в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.drawing/shape/get_hasimage/
---
## Shape::get_HasImage method


Возвращает **true**, если у фигуры есть байты изображения или она ссылается на изображение.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasImage()
```


## Примеры



Показывает, как извлекать изображения из документа и сохранять их в локальную файловую систему как отдельные файлы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Получите коллекцию фигур из документа,
// и сохраните данные изображения каждой фигуры, содержащей изображение, в файл на локальной файловой системе.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // Данные изображений фигур могут содержать изображения во множестве возможных форматов.
        // Мы можем автоматически определить расширение файла для каждого изображения, исходя из его формата.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


Показывает, как удалить из документа все фигуры с изображениями.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));

for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        shape->Remove();
    }
}

ASSERT_EQ(0, shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));
```

## См. также

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
