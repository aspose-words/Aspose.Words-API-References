---
title: "Aspose::Words::Drawing::ImageData::Save metodu"
linktitle: "Save"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageData::Save metodu. Görüntüyü C++'da belirtilen akışa kaydeder."
type: docs
weight: 22000
url: /tr/cpp/aspose.words.drawing/imagedata/save/
---
## ImageData::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Görüntüyü belirtilen akışa kaydeder.

```cpp
void Aspose::Words::Drawing::ImageData::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Görüntünün kaydedileceği akış. |
## Açıklamalar


Akış nesnesini serbest bırakmak çağıranın sorumluluğu mudur?

## Ayrıca Bakınız

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::Save(const System::String\&) method


Görüntüyü bir dosyaya kaydeder.

```cpp
void Aspose::Words::Drawing::ImageData::Save(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Görüntünün kaydedileceği dosya adı. |

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

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::ImageData::Save(std::basic_ostream<CharType, Traits> &stream)
```

## Ayrıca Bakınız

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
