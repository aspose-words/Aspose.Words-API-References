---
title: "Aspose::Words::Drawing::Shape::get_HasImage yöntemi"
linktitle: "get_HasImage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Shape::get_HasImage yöntemi. Şeklin görüntü baytları varsa veya bir görüntüye bağlanıyorsa C++ içinde true döndürür."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.drawing/shape/get_hasimage/
---
## Shape::get_HasImage method


Returns **true** if the shape has image bytes or links an image.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasImage()
```


## Örnekler



Bir belgeden görüntülerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı ayrı dosyalar olarak nasıl kaydedileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Belgeden şekil koleksiyonunu alın,
// ve görüntüsü olan her şeklin görüntü verisini bir dosya olarak yerel dosya sistemine kaydedin.
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
        // Şekillerin görüntü verileri birçok olası görüntü formatında görüntüler içerebilir.
        // Her görüntü için dosya uzantısını, formatına göre otomatik olarak belirleyebiliriz.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


Bir belgede bulunan tüm görüntülü şekilleri nasıl sileceğinizi gösterir.
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

## Ayrıca Bakınız

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
