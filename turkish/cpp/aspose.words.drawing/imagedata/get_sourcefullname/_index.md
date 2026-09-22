---
title: "Aspose::Words::Drawing::ImageData::get_SourceFullName metodu"
linktitle: "get_SourceFullName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageData::get_SourceFullName metodu. Bağlantılı görüntü için kaynak dosyanın yolunu ve adını C++'da alır veya ayarlar."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.drawing/imagedata/get_sourcefullname/
---
## ImageData::get_SourceFullName method


Bağlı görüntünün kaynak dosyasının yolunu ve adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Drawing::ImageData::get_SourceFullName()
```

## Açıklamalar


Varsayılan değer boş bir dizedir.

Eğer [SourceFullName](./) boş bir dize değilse, görüntü bağlantılıdır.

## Örnekler



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

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
