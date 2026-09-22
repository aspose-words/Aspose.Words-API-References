---
title: "Aspose::Words::FileFormatUtil::ImageTypeToExtension metodu"
linktitle: "ImageTypeToExtension"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FileFormatUtil::ImageTypeToExtension metodu. Bir Aspose.Words görüntü türü numaralandırılmış değerini dosya uzantısına dönüştürür. Döndürülen uzantı, C++'ta başında nokta bulunan küçük harfli bir dizedir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil::ImageTypeToExtension method


Bir Aspose.Words görüntü tipi enum değerini bir dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir.

```cpp
static System::String Aspose::Words::FileFormatUtil::ImageTypeToExtension(Aspose::Words::Drawing::ImageType imageType)
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

## Ayrıca Bakınız

* Enum [ImageType](../../../aspose.words.drawing/imagetype/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
