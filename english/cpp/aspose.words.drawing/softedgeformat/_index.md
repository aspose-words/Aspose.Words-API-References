---
title: Aspose::Words::Drawing::SoftEdgeFormat class
linktitle: SoftEdgeFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::SoftEdgeFormat class. Represents the soft edge formatting for an object in C++.'
type: docs
weight: 13500
url: /cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


Represents the soft edge formatting for an object.

```cpp
class SoftEdgeFormat : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Radius](./get_radius/)() | Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt). The default value is 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Removes [SoftEdgeFormat](./) from the parent object. |
| [set_Radius](./set_radius/)(double) | Setter for [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/). |
| static [Type](./type/)() |  |
## Remarks


Use the [SoftEdge](../shapebase/get_softedge/) property to access soft edge properties of an object. You do not create instances of the [SoftEdgeFormat](./) class directly.

## Examples



Shows how to work with soft edge formatting. 
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Apply soft edge to the shape.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Load document with rectangle shape with soft edge.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Check soft edge radius.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Remove soft edge from the shape.
softEdgeFormat->Remove();

// Check radius of the removed soft edge.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
