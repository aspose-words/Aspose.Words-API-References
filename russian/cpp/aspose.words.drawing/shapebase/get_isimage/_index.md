---
title: "метод Aspose::Words::Drawing::ShapeBase::get_IsImage"
linktitle: "get_IsImage"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Drawing::ShapeBase::get_IsImage. Возвращает true, если эта форма является изображением, в C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words.drawing/shapebase/get_isimage/
---
## ShapeBase::get_IsImage method


Возвращает **true**, если эта фигура является изображением.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsImage()
```


## Примеры



Показывает, как открыть HTML‑документ с изображениями из потока, используя базовый URI.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Передайте URI базовой папки при загрузке.
    // чтобы любые изображения с относительными URI в HTML‑документе могли быть найдены.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Убедитесь, что первая фигура документа содержит действительное изображение.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
