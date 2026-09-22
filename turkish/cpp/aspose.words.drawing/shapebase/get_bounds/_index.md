---
title: "Aspose::Words::Drawing::ShapeBase::get_Bounds metodu"
linktitle: "get_Bounds"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_Bounds metodu. C++'ta şeklin içinde bulunduğu bloğun konumunu ve boyutunu alır veya ayarlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.drawing/shapebase/get_bounds/
---
## ShapeBase::get_Bounds method


Şeklin içinde bulunduğu bloğun konumunu ve boyutunu alır veya ayarlar.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_Bounds()
```

## Açıklamalar


Ayarlandığında en-boy oranı kilidini yok sayar.

Üst düzey bir şekil için değer, puan cinsindendir ve şekil çapa noktasına göre görecelidir.

Bir grup içindeki şekiller için değer, ebeveyn grubunun koordinat uzayında ve birimlerinde bulunur.

## Örnekler



Bir grup şekli oluşturmayı ve doldurmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir grup şekli oluşturun. Grup şekli, çocuk şekil düğümlerinin bir koleksiyonunu görüntüleyebilir.
// Microsoft Word'de, grup şeklinin sınırları içinde veya grup şeklinin bir çocuk şekline tıklamak,
// bu grup içindeki diğer tüm çocuk şekilleri seçer ve tüm şekilleri aynı anda ölçeklendirmemize ve taşımamıza izin verir.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);

ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, group->get_WrapType());

// 400pt x 400pt boyutunda bir grup şekli oluşturun ve belge'nin yüzen şekil koordinat başlangıcına yerleştirin.
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// Grubun iç koordinat düzlemi boyutunu 500 x 500pt olarak ayarlayın.
// Grubun sol üst köşesi (0, 0) x ve y koordinatına sahip olacaktır,
// ve sağ alt köşe (500, 500) x ve y koordinatına sahip olacaktır.
group->set_CoordSize(System::Drawing::Size(500, 500));

// Grubun sol üst köşesinin koordinatlarını (-250, -250) olarak ayarlayın.
// Grubun merkezi artık (0, 0) x ve y koordinat değerine sahip olacak,
// ve sağ alt köşe (250, 250) konumunda olacak.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// Bu grup şeklinin sınırını gösterecek bir dikdörtgen oluşturun ve gruba ekleyin.
auto child1 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child1->set_Width(group->get_CoordSize().get_Width());
child1->set_Height(group->get_CoordSize().get_Height());
child1->set_Left(group->get_CoordOrigin().get_X());
child1->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child1);

// Bir şekil grup şeklinin bir parçası olduğunda, ona bir çocuk düğüm olarak erişebilir ve ardından değiştirebiliriz.
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::Dash);

// Küçük bir kırmızı yıldız oluşturun ve gruba ekleyin.
// Şekli, merkezine taşıdığımız grup koordinat orijiniyle hizalayın.
auto child2 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Star);
child2->set_Width(20);
child2->set_Height(20);
child2->set_Left(-10);
child2->set_Top(-10);
child2->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child2);

// Bir dikdörtgen ekleyin ve ardından aynı konuma bir görüntülü, biraz daha küçük bir dikdörtgen ekleyin.
// Gruba eklediğimiz yeni şekiller eski şekillerin üzerine biner. Açık mavi dikdörtgen kırmızı yıldızın bir kısmını örtüp geçecek,
// ve ardından görüntülü şekil, açık mavi dikdörtgenin üzerine çerçeve olarak yerleştirerek geçecek.
// Şekillerin "ZOrder" özelliklerini grup şekli içinde düzenlerini değiştirmek için kullanamayız.
auto child3 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child3->set_Width(250);
child3->set_Height(250);
child3->set_Left(-250);
child3->set_Top(-250);
child3->set_FillColor(System::Drawing::Color::get_LightBlue());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child3);

auto child4 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
child4->set_Width(200);
child4->set_Height(200);
child4->set_Left(-225);
child4->set_Top(-225);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child4);

(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 3, true)))->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Grup şekline bir metin kutusu ekleyin. Metin kutusunun sağ kenarı "Left" özelliğiyle ayarlayın
// grup şeklinin sağ sınırına dokunsun. Metin kutusunun dışarıda durması için "Top" özelliğini ayarlayın
// grup şeklinin sınırına, üst kısmı grup şeklinin alt kenarıyla hizalanacak şekilde.
auto child5 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
child5->set_Width(200);
child5->set_Height(50);
child5->set_Left(group->get_CoordSize().get_Width() + group->get_CoordOrigin().get_X() - 200);
child5->set_Top(group->get_CoordSize().get_Height() + group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child5);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(group);
builder->MoveTo((System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 4, true)))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Shape.GroupShape.docx");
```


Şeklin içerik bloğu sınırlarını nasıl doğrulayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// Satır kendisi belge sayfasında çok az yer kaplasa da,
// dikdörtgen bir içerik bloğu kaplar ve bu bloğun boyutunu "Bounds" özelliklerini kullanarak belirleyebiliriz.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// Bir grup şekil oluşturun ve ardından "Bounds" özelliğini kullanarak içerik bloğunun boyutunu ayarlayın.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// Bir dikdörtgen oluşturun, sınırlayıcı bloğunun boyutunu doğrulayın ve ardından grup şekline ekleyin.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Grup şeklinin koordinat düzlemi, içerik bloğunun sol üst köşesinde bir orijine sahiptir,
// ve (1000, 1000) koordinatları sağ alt köşededir.
// Grup şeklimiz 250x250pt boyutundadır, bu yüzden grup şeklinin koordinat düzlemindeki her 4pt
// belge gövdesinin koordinat düzleminde 1pt'ye karşılık gelir.
// Eklediğimiz her şekil de boyut olarak 4 kat küçülecektir.
// Şeklin "BoundsInPoints" özelliğindeki değişiklik bunu yansıtacaktır.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// Bir şekil ekleyin ve onu grup şeklinin içerik bloğu sınırlarının dışına yerleştirin.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Grup şeklinin belge gövdesindeki ayak izi arttı, ancak içerik bloğu aynı kaldı.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
