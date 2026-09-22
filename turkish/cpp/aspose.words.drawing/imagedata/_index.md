---
title: "Aspose::Words::Drawing::ImageData class"
linktitle: "ImageData"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageData class. Defines an image for a shape. To learn more, visit the  documentation article in C++."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.drawing/imagedata/
---
## ImageData class


Bir şekil için görüntüyü tanımlar. Daha fazla bilgi için, [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/) dokümantasyon makalesini ziyaret edin.

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [FitImageToShape](./fitimagetoshape/)() | Fits the image data to [Shape](../shape/) frame so that the aspect ratio of the image data matches the aspect ratio of [Shape](../shape/) frame. |
| [get_BiLevel](./get_bilevel/)() | Determines whether an image will be displayed in black and white. |
| [get_Borders](./get_borders/)() | Gets the collection of borders of the image. Borders only have effect for inline images. |
| [get_Brightness](./get_brightness/)() | Gets or sets the brightness of the picture. The value for this property must be a number from 0.0 (dimmest) to 1.0 (brightest). |
| [get_ChromaKey](./get_chromakey/)() | Defines the color value of the image that will be treated as transparent. |
| [get_Contrast](./get_contrast/)() | Gets or sets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast). |
| [get_CropBottom](./get_cropbottom/)() | Defines the fraction of picture removal from the bottom side. |
| [get_CropLeft](./get_cropleft/)() | Defines the fraction of picture removal from the left side. |
| [get_CropRight](./get_cropright/)() | Defines the fraction of picture removal from the right side. |
| [get_CropTop](./get_croptop/)() | Defines the fraction of picture removal from the top side. |
| [get_GrayScale](./get_grayscale/)() | Determines whether a picture will display in grayscale mode. |
| [get_HasImage](./get_hasimage/)() | Returns **true** if the shape has image bytes or links an image. |
| [get_ImageBytes](./get_imagebytes/)() | Şekilde depolanan görüntünün ham baytlarını alır veya ayarlar. |
| [get_ImageSize](./get_imagesize/)() | Görüntü boyutu ve çözünürlüğü hakkında bilgileri alır. |
| [get_ImageType](./get_imagetype/)() | Görüntünün türünü alır. |
| [get_IsLink](./get_islink/)() | Görüntü şekle bağlıysa **true** döndürür ([SourceFullName](./get_sourcefullname/) belirtildiğinde). |
| [get_IsLinkOnly](./get_islinkonly/)() | Görüntü bağlıysa ve belgede depolanmamışsa **true** döndürür. |
| [get_SourceFullName](./get_sourcefullname/)() | Bağlı görüntünün kaynak dosyasının yolunu ve adını alır veya ayarlar. |
| [get_Title](./get_title/)() | Bir görüntünün başlığını tanımlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Görüntüyü belirtilen akışa kaydeder. |
| [Save](./save/)(const System::String\&) | Görüntüyü bir dosyaya kaydeder. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/) için ayarlayıcı. |
| [set_Brightness](./set_brightness/)(double) | [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/) için ayarlayıcı. |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/) için ayarlayıcı. |
| [set_Contrast](./set_contrast/)(double) | [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/) için ayarlayıcı. |
| [set_CropBottom](./set_cropbottom/)(double) | [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/) için ayarlayıcı. |
| [set_CropLeft](./set_cropleft/)(double) | [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/) için ayarlayıcı. |
| [set_CropRight](./set_cropright/)(double) | [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/) için ayarlayıcı. |
| [set_CropTop](./set_croptop/)(double) | [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/) için ayarlayıcı. |
| [set_GrayScale](./set_grayscale/)(bool) | [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/) için ayarlayıcı. |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/) için ayarlayıcı. |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/) için ayarlayıcı. |
| [set_Title](./set_title/)(const System::String\&) | [Aspose::Words::Drawing::ImageData::get_Title](./get_title/) için ayarlayıcı. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Şeklin gösterdiği görüntüyü ayarlar. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Şeklin gösterdiği görüntüyü ayarlar. |
| [SetImage](./setimage/)(const System::String\&) | Şeklin gösterdiği görüntüyü ayarlar. |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | Görüntünün depolanmış ya da bağlı olup olmadığına bakılmaksızın herhangi bir görüntünün baytlarını döndürür. |
| [ToImage](./toimage/)() | Şekilde depolanan görüntüyü **Image** nesnesi olarak alır. |
| [ToStream](./tostream/)() | Görüntü baytlarını içeren bir akış oluşturur ve döndürür. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir şeklin içindeki görüntüye erişmek ve onu değiştirmek için [ImageData](../shape/get_imagedata/) özelliğini kullanın. [ImageData](./) sınıfının örneklerini doğrudan oluşturmazsınız.

Bir görüntü bir şeklin içinde depolanabilir, harici bir dosyaya bağlanabilir veya her ikisi birden (bağlantılı ve belgede depolanmış) olabilir.

Görüntünün şeklin içinde depolanıp depolanmadığına veya bağlanıp bağlanmadığına bakılmaksızın, gerçek görüntüye her zaman [ToByteArray](./tobytearray/), [ToStream](./tostream/), [ToImage](./toimage/) veya [Save()](../) yöntemlerini kullanarak erişebilirsiniz. Görüntü şeklin içinde depolanmışsa, [ImageBytes](./get_imagebytes/) özelliğini kullanarak da doğrudan erişebilirsiniz.

Bir görüntüyü bir şeklin içinde depolamak için [SetImage()](../) yöntemini kullanın. Bir görüntüyü bir şekle bağlamak için ise [SourceFullName](./get_sourcefullname/) özelliğini ayarlayın.

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


Bağlantılı bir görüntünün belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// Aşağıda bir görüntünün bir şekle uygulanarak görüntülenebilmesi için iki yöntem bulunmaktadır.
// 1 -  Şekli görüntüyü içerecek şekilde ayarlayın.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// Şekilde depoladığımız her görüntü, belgemizin boyutunu artıracaktır.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  Şekli yerel dosya sistemindeki bir görüntü dosyasına bağlayacak şekilde ayarlayın.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// Görüntülere bağlanmak alan tasarrufu sağlar ve daha küçük bir belgeyle sonuçlanır.
// Ancak, belge yalnızca görüntüyü doğru bir şekilde gösterebilir
// görüntü dosyası, şeklin "SourceFullName" özelliğinin işaret ettiği konumda mevcut olduğu sürece.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
