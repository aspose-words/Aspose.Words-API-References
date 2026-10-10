---
title: "Aspose::Words::Drawing::Stroke::get_BaseForeColor méthode"
linktitle: "get_BaseForeColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Stroke::get_BaseForeColor méthode. Obtient la couleur de premier plan de base du trait sans aucun modificateur en C++."
type: docs
weight: 2500
url: /fr/cpp/aspose.words.drawing/stroke/get_baseforecolor/
---
## Stroke::get_BaseForeColor method


Obtient la couleur de premier plan de base du trait sans aucun modificateur.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Stroke::get_BaseForeColor()
```


## Exemples



Montre comment obtenir la couleur de premier plan sans modificateurs.
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

## Voir aussi

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
