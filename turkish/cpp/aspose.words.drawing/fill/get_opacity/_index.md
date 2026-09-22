---
title: "Aspose::Words::Drawing::Fill::get_Opacity metodu"
linktitle: "get_Opacity"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::get_Opacity metodu. C++'ta belirtilen doldurmanın opaklık derecesini 0.0 (şeffaf) ile 1.0 (opak) arasında bir değer olarak alır veya ayarlar."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.drawing/fill/get_opacity/
---
## Fill::get_Opacity method


Belirtilen dolgunun opaklık derecesini 0.0 (şeffaf) ile 1.0 (opak) arasında bir değer olarak alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::Fill::get_Opacity()
```


## Örnekler



Bir şekli katı bir renk ile doldurmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Biraz metin yazın ve ardından onu yüzen bir şekille kapatın.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Use the "StrokeColor" özelliğini kullanarak şeklin dış kenarının rengini ayarlayın.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Use the "FillColor" özelliğini kullanarak şeklin iç bölgesinin rengini ayarlayın.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// "Opacity" özelliği, rengin 0-1 ölçeğinde ne kadar şeffaf olduğunu belirler,
// 1 tamamen opak, 0 ise görünmez olur.
// Şekil dolgu varsayılan olarak tamamen opaktır, bu yüzden bu şeklin üstünde olduğu metni göremiyoruz.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Şekil dolgu renginin opaklığını daha düşük bir değere ayarlayın, böylece altındaki metni görebiliriz.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Ayrıca Bakınız

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
