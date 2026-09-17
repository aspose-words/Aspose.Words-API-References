---
title: "Méthode Aspose::Words::Drawing::Fill::get_Opacity"
linktitle: "get_Opacity"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Fill::get_Opacity. Obtient ou définit le degré d'opacité du remplissage spécifié comme une valeur comprise entre 0,0 (transparent) et 1,0 (opaque) en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.drawing/fill/get_opacity/
---
## Fill::get_Opacity method


Obtient ou définit le degré d'opacité du remplissage spécifié comme une valeur comprise entre 0.0 (transparent) et 1.0 (opaque).

```cpp
double Aspose::Words::Drawing::Fill::get_Opacity()
```


## Exemples



Montre comment remplir une forme avec une couleur unie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Écrivez du texte, puis recouvrez-le d'une forme flottante.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Utilisez la propriété "StrokeColor" pour définir la couleur du contour de la forme.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Utilisez la propriété "FillColor" pour définir la couleur de la zone intérieure de la forme.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// La propriété "Opacity" détermine la transparence de la couleur sur une échelle de 0 à 1,
// 1 étant totalement opaque, et 0 étant invisible.
// Le remplissage de la forme est, par défaut, totalement opaque, donc nous ne pouvons pas voir le texte sur lequel cette forme se trouve.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Réglez l'opacité de la couleur de remplissage de la forme à une valeur plus basse afin que nous puissions voir le texte en dessous.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Voir aussi

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
