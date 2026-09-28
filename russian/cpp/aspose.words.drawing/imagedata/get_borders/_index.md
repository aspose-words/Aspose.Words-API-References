---
title: "Aspose::Words::Drawing::ImageData::get_Borders метод"
linktitle: "get_Borders"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ImageData::get_Borders метод. Получает коллекцию границ изображения. Границы влияют только на встроенные изображения в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing/imagedata/get_borders/
---
## ImageData::get_Borders method


Получает коллекцию границ изображения. Границы влияют только на встроенные изображения.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::Drawing::ImageData::get_Borders()
```


## Примеры



Показывает, как редактировать данные изображения фигуры.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
auto sourceShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

auto dstDoc = System::MakeObject<Aspose::Words::Document>();

// Импортируйте фигуру из исходного документа и добавьте её в первый абзац.
auto importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

// Импортированная фигура содержит изображение. Мы можем получить доступ к свойствам изображения и его сырым данным через объект ImageData.
System::SharedPtr<Aspose::Words::Drawing::ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// Если у изображения нет границ, его объект ImageData определит цвет границы как пустой.
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// Это изображение не ссылается на другую фигуру или файл изображения в локальной файловой системе.
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// Свойства "Brightness" и "Contrast" определяют яркость и контраст изображения.
// по шкале от 0 до 1, со значением по умолчанию 0,5.
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// Указанные выше значения яркости и контраста создали изображение с большим количеством белого.
// Мы можем выбрать цвет с помощью свойства ChromaKey для замены его на прозрачность, например белый.
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// Снова импортируйте исходную фигуру и установите изображение в монохромный режим.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// Снова импортируйте исходную фигуру, чтобы создать третье изображение, и установите его в режим BiLevel.
// BiLevel устанавливает каждый пиксель либо в черный, либо в белый цвет, в зависимости от того, какой из них ближе к исходному цвету.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// Обрезка определяется по шкале от 0-1. Обрезка стороны на 0.3
// будет обрезать 30% изображения со стороны, где выполнена обрезка.
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(get_ArtifactsDir() + u"Drawing.ImageData.docx");
```

## См. также

* Class [BorderCollection](../../../aspose.words/bordercollection/)
* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
