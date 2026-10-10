---
title: "Aspose::Words::Drawing::Shape::get_ImageData metodu"
linktitle: "get_ImageData"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Shape::get_ImageData metodu. Şeklin görüntüsüne erişim sağlar. Şeklin C++'ta bir görüntüsü olamazsa null döndürür."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.drawing/shape/get_imagedata/
---
## Shape::get_ImageData method


Şeklin görüntüsüne erişim sağlar. Şeklin görüntüsü olamazsa **null** döndürür.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ImageData> Aspose::Words::Drawing::Shape::get_ImageData()
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

* Class [ImageData](../../imagedata/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
