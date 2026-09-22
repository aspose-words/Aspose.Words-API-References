---
title: "Aspose::Words::Drawing::ShapeBase::get_IsImage metodu"
linktitle: "get_IsImage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_IsImage metodu. Bu şekil bir görüntü şekli ise C++'ta true döndürür."
type: docs
weight: 29000
url: /tr/cpp/aspose.words.drawing/shapebase/get_isimage/
---
## ShapeBase::get_IsImage method


Bu şekil bir resim şekli ise **true** döndürür.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsImage()
```


## Örnekler



Bir akıştan temel URI kullanarak görüntülü bir HTML belgesinin nasıl açılacağını gösterir.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Yüklerken temel klasörün URI'sını geçirin
    // böylece HTML belgesindeki göreli URI'li tüm görüntüler bulunabilir.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Belgenin ilk şeklinin geçerli bir görüntü içerdiğini doğrulayın.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
