---
title: "Aspose::Words::Drawing::Fill::get_BaseForeColor yöntemi"
linktitle: "get_BaseForeColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::get_BaseForeColor yöntemi. C++'da doldurma için herhangi bir değiştirici olmadan temel ön plan rengini temsil eden bir Color nesnesi alır."
type: docs
weight: 4500
url: /tr/cpp/aspose.words.drawing/fill/get_baseforecolor/
---
## Fill::get_BaseForeColor method


Herhangi bir değiştirici olmadan dolgu için temel ön plan rengini temsil eden bir Color nesnesini alır.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_BaseForeColor()
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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
