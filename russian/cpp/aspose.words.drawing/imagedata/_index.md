---
title: "Aspose::Words::Drawing::ImageData класс"
linktitle: "ImageData"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ImageData класс. Определяет изображение для фигуры. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.drawing/imagedata/
---
## ImageData class


Определяет изображение для фигуры. Чтобы узнать больше, посетите статью документации [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [FitImageToShape](./fitimagetoshape/)() | Подгоняет данные изображения к кадру [Shape](../shape/), так чтобы соотношение сторон данных изображения совпадало с соотношением сторон кадра [Shape](../shape/). |
| [get_BiLevel](./get_bilevel/)() | Определяет, будет ли изображение отображаться в чёрно‑белом виде. |
| [get_Borders](./get_borders/)() | Получает коллекцию границ изображения. Границы влияют только на встроенные изображения. |
| [get_Brightness](./get_brightness/)() | Получает или задаёт яркость изображения. Значение этого свойства должно быть числом от 0,0 (самое тёмное) до 1,0 (самое яркое). |
| [get_ChromaKey](./get_chromakey/)() | Определяет цветовое значение изображения, которое будет считаться прозрачным. |
| [get_Contrast](./get_contrast/)() | Получает или задаёт контраст указанного изображения. Значение этого свойства должно быть числом от 0,0 (наименьший контраст) до 1,0 (наибольший контраст). |
| [get_CropBottom](./get_cropbottom/)() | Определяет долю обрезки изображения снизу. |
| [get_CropLeft](./get_cropleft/)() | Определяет долю обрезки изображения слева. |
| [get_CropRight](./get_cropright/)() | Определяет долю обрезки изображения справа. |
| [get_CropTop](./get_croptop/)() | Определяет долю обрезки изображения сверху. |
| [get_GrayScale](./get_grayscale/)() | Определяет, будет ли изображение отображаться в режиме градаций серого. |
| [get_HasImage](./get_hasimage/)() | Возвращает **true**, если у фигуры есть байты изображения или она ссылается на изображение. |
| [get_ImageBytes](./get_imagebytes/)() | Получает или задает необработанные байты изображения, хранящиеся в фигуре. |
| [get_ImageSize](./get_imagesize/)() | Получает информацию о размере изображения и разрешении. |
| [get_ImageType](./get_imagetype/)() | Получает тип изображения. |
| [get_IsLink](./get_islink/)() | Возвращает **true**, если изображение связано с фигурой (когда указано [SourceFullName](./get_sourcefullname/)). |
| [get_IsLinkOnly](./get_islinkonly/)() | Возвращает **true**, если изображение связано и не хранится в документе. |
| [get_SourceFullName](./get_sourcefullname/)() | Получает или задает путь и имя исходного файла для связанного изображения. |
| [get_Title](./get_title/)() | Определяет заголовок изображения. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сохраняет изображение в указанный поток. |
| [Save](./save/)(const System::String\&) | Сохраняет изображение в файл. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | Сеттер для [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/). |
| [set_Brightness](./set_brightness/)(double) | Сеттер для [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/). |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/). |
| [set_Contrast](./set_contrast/)(double) | Сеттер для [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/). |
| [set_CropBottom](./set_cropbottom/)(double) | Сеттер для [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/). |
| [set_CropLeft](./set_cropleft/)(double) | Сеттер для [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/). |
| [set_CropRight](./set_cropright/)(double) | Сеттер для [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/). |
| [set_CropTop](./set_croptop/)(double) | Сеттер для [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/). |
| [set_GrayScale](./set_grayscale/)(bool) | Сеттер для [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/). |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | Сеттер для [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/). |
| [set_Title](./set_title/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::ImageData::get_Title](./get_title/). |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Устанавливает изображение, которое отображает фигура. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Устанавливает изображение, которое отображает фигура. |
| [SetImage](./setimage/)(const System::String\&) | Устанавливает изображение, которое отображает фигура. |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | Возвращает байты изображения для любого изображения независимо от того, хранится ли изображение или связано. |
| [ToImage](./toimage/)() | Получает изображение, хранящееся в фигуре, как объект **Image**. |
| [ToStream](./tostream/)() | Создаёт и возвращает поток, содержащий байты изображения. |
| static [Type](./type/)() |  |
## Примечания


Используйте свойство [ImageData](../shape/get_imagedata/) для доступа к изображению внутри фигуры и его изменения. Вы не создаёте экземпляры класса [ImageData](./) напрямую.

Изображение может быть сохранено внутри фигуры, привязано к внешнему файлу или оба варианта одновременно (привязано и сохранено в документе).

Независимо от того, сохранено ли изображение внутри фигуры или привязано, вы всегда можете получить доступ к реальному изображению с помощью методов [ToByteArray](./tobytearray/), [ToStream](./tostream/), [ToImage](./toimage/) или [Save()](../). Если изображение сохранено внутри фигуры, вы также можете напрямую получить к нему доступ через свойство [ImageBytes](./get_imagebytes/).

Чтобы сохранить изображение внутри фигуры, используйте метод [SetImage()](../). Чтобы привязать изображение к фигуре, задайте свойство [SourceFullName](./get_sourcefullname/).

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


Показывает, как вставить привязанное изображение в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// Ниже представлены два способа применения изображения к фигуре, чтобы она могла его отображать.
// 1 - Установите фигуру так, чтобы она содержала изображение.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// Каждое изображение, которое мы сохраняем в фигуре, увеличивает размер нашего документа.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 - Установите фигуру так, чтобы она ссылалась на файл изображения в локальной файловой системе.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// Привязка к изображениям экономит место и приводит к меньшему размеру документа.
// Однако документ может корректно отображать изображение только пока
// файл изображения присутствует по пути, на который указывает свойство \"SourceFullName\" фигуры.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
