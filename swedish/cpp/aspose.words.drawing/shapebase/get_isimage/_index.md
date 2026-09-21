---
title: "Aspose::Words::Drawing::ShapeBase::get_IsImage metod"
linktitle: "get_IsImage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_IsImage metod. Returnerar true om denna form är en bildform i C++."
type: docs
weight: 29000
url: /sv/cpp/aspose.words.drawing/shapebase/get_isimage/
---
## ShapeBase::get_IsImage method


Returnerar **true** om denna form är en bildform.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsImage()
```


## Exempel



Visar hur man öppnar ett HTML-dokument med bilder från en ström med hjälp av en bas-URI.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Skicka med URI:n för basmappen när du laddar den
    // så att eventuella bilder med relativa URI:er i HTML-dokumentet kan hittas.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Verifiera att den första formen i dokumentet innehåller en giltig bild.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
