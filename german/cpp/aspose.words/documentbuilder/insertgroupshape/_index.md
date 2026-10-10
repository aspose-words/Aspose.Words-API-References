---
title: "Aspose::Words::DocumentBuilder::InsertGroupShape‑Methode"
linktitle: "InsertGroupShape"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertGroupShape‑Methode. Gruppiert die als Parameter übergebenen Shapes in einen neuen GroupShape‑Knoten, der an der aktuellen Position in C++ eingefügt wird."
type: docs
weight: 35500
url: /de/cpp/aspose.words/documentbuilder/insertgroupshape/
---
## DocumentBuilder::InsertGroupShape(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


Gruppiert die als Parameter übergebenen Formen in einen neuen GroupShape‑Knoten, der an der aktuellen Position eingefügt wird.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Formen | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | Die Liste der zu gruppierenden Shapes. |
## Hinweise


Die Position und Dimension der neuen GroupShape wird automatisch berechnet.

VML- und DML-Formen können nicht zusammen gruppiert werden.

## Beispiele



Zeigt, wie man eine DML-Gruppenform einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 250);
shape1->set_Left(20);
shape1->set_Top(20);
shape1->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 150, 200);
shape2->set_Left(40);
shape2->set_Top(50);
shape2->get_Stroke()->set_Color(System::Drawing::Color::get_Green());

// Abmessungen für den neuen GroupShape-Knoten.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Fügen Sie einen GroupShape-Knoten für die angegebene Größe ein, der an der angegebenen Position platziert wird.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// Fügen Sie einen GroupShape-Knoten ein, dessen Position und Dimension automatisch berechnet werden.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```


Zeigt, wie man eine Gruppenform mit der Form kombiniert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 250);
shape1->set_Left(20);
shape1->set_Top(20);
shape1->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 150, 200);
shape2->set_Left(40);
shape2->set_Top(50);
shape2->get_Stroke()->set_Color(System::Drawing::Color::get_Green());

// Kombinieren Sie Formen zu einem GroupShape-Knoten, der an der angegebenen Position eingefügt wird.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape1, shape2}));

// Kombinieren Sie Shape- und GroupShape-Knoten.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({groupShape1, shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.CombineGroupShape.docx");
```

## Siehe auch

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertGroupShape(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


Gruppiert die als Parameter übergebenen Formen in einen neuen GroupShape-Knoten der angegebenen Größe, der an der angegebenen Position eingefügt wird.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(double left, double top, double width, double height, const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| left | double | Abstand in Punkten vom Ursprung zur linken Seite der Gruppenform. |
| top | double | Abstand in Punkten vom Ursprung zur oberen Seite der Gruppenform. |
| Breite | double | Die Breite der Gruppenform in Punkten. Ein negativer Wert ist nicht zulässig. |
| Höhe | double | Die Höhe der Gruppenform in Punkten. Ein negativer Wert ist nicht zulässig. |
| Formen | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | Die Liste der zu gruppierenden Shapes. |

## Beispiele



Zeigt, wie man eine DML-Gruppenform einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 250);
shape1->set_Left(20);
shape1->set_Top(20);
shape1->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 150, 200);
shape2->set_Left(40);
shape2->set_Top(50);
shape2->get_Stroke()->set_Color(System::Drawing::Color::get_Green());

// Abmessungen für den neuen GroupShape-Knoten.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Fügen Sie einen GroupShape-Knoten für die angegebene Größe ein, der an der angegebenen Position platziert wird.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// Fügen Sie einen GroupShape-Knoten ein, dessen Position und Dimension automatisch berechnet werden.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```

## Siehe auch

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
