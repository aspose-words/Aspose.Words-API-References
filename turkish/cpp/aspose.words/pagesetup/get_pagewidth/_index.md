---
title: "Aspose::Words::PageSetup::get_PageWidth metodu"
linktitle: "get_PageWidth"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_PageWidth yöntemi. Sayfanın genişliğini nokta cinsinden döndürür veya ayarlar C++'ta."
type: docs
weight: 36000
url: /tr/cpp/aspose.words/pagesetup/get_pagewidth/
---
## PageSetup::get_PageWidth method


Sayfanın genişliğini nokta cinsinden döndürür veya ayarlar.

```cpp
double Aspose::Words::PageSetup::get_PageWidth()
```


## Örnekler



Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Görüntüyü başlığa ekleyin, böylece her sayfada görünür.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Görüntüyü sayfanın ortasına yerleştirin.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


Yüzen bir görüntünün nasıl ekleneceğini ve konumunun ve boyutunun nasıl belirtileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Şeklin "RelativeHorizontalPosition" özelliğini, "Left" özelliğinin değerini şeklin yatay uzaklığı olarak ele alacak şekilde yapılandırın
// sayfanın sol tarafından, nokta cinsinden, şeklin yatay uzaklığı olarak.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Şeklin sayfanın sol tarafından yatay uzaklığını 100'e ayarlayın.
shape->set_Left(100);

// "RelativeVerticalPosition" özelliğini benzer bir şekilde kullanarak şekli sayfanın üstünden 80pt aşağı konumlandırın.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Şeklin yüksekliğini ayarlayın; bu, boyutları korumak için genişliği otomatik olarak ölçeklendirecektir.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// "Bottom" ve "Right" özellikleri, görüntünün alt ve sağ kenarlarını içerir.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
