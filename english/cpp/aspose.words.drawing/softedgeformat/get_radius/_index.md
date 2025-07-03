---
title: Aspose::Words::Drawing::SoftEdgeFormat::get_Radius method
linktitle: get_Radius
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::SoftEdgeFormat::get_Radius method. Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt). The default value is 0.0 in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.drawing/softedgeformat/get_radius/
---
## SoftEdgeFormat::get_Radius method


Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt). The default value is 0.0.

```cpp
double Aspose::Words::Drawing::SoftEdgeFormat::get_Radius()
```


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


Shows how to set limit for image resolution. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## See Also

* Class [SoftEdgeFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
