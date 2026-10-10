---
title: "Aspose::Words::Drawing::Stroke::get_BaseForeColor metodu"
linktitle: "get_BaseForeColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Stroke::get_BaseForeColor metodu. C++'da çizginin temel ön plan rengini, herhangi bir değiştirici olmadan alır."
type: docs
weight: 2500
url: /tr/cpp/aspose.words.drawing/stroke/get_baseforecolor/
---
## Stroke::get_BaseForeColor method


Çizginin temel ön plan rengini, herhangi bir değiştirici olmadan alır.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Stroke::get_BaseForeColor()
```


## Örnekler



Değiştiriciler olmadan ön plan renginin nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
shape->get_Fill()->set_ForeTintAndShade(0.5);
shape->get_Stroke()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());
shape->get_Stroke()->get_Fill()->set_Transparency(0.5);

ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 188, 188).ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_BaseForeColor().ToArgb());

ASSERT_EQ(System::Drawing::Color::FromArgb(128, 0, 128, 0).ToArgb(), shape->get_Stroke()->get_ForeColor().ToArgb());
ASSERT_EQ(System::Drawing::Color::get_Green().ToArgb(), shape->get_Stroke()->get_BaseForeColor().ToArgb());

ASSERT_EQ(System::Drawing::Color::get_Green().ToArgb(), shape->get_Stroke()->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(System::Drawing::Color::get_Green().ToArgb(), shape->get_Stroke()->get_Fill()->get_BaseForeColor().ToArgb());
```

## Ayrıca Bakınız

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
