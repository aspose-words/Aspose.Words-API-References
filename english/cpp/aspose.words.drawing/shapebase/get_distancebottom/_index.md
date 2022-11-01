---
title: get_DistanceBottom
second_title: Aspose.Words for C++ API Reference
description: Returns or sets the distance (in points) between the document text and the bottom edge of the shape.
type: docs
weight: 170
url: /cpp/aspose.words.drawing/shapebase/get_distancebottom/
---
## ShapeBase.get_DistanceBottom method


Returns or sets the distance (in points) between the document text and the bottom edge of the shape.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceBottom()
```


The default value is 0.

Has effect only for top level shapes.

## Examples




Shows how to set the wrapping distance for a text that surrounds a shape. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a rectangle and, get the text to wrap tightly around its bounds.
SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Rectangle, 150, 150);
shape->set_WrapType(WrapType::Tight);

// Set the minimum distance between the shape and surrounding text to 40pt from all sides.
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// Move the shape closer to the center of the page, and then rotate the shape 60 degrees clockwise.
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// Add text that will wrap around the shape.
builder->get_Font()->set_Size(24);
builder->Write(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") +
               u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(ArtifactsDir + u"Shape.Coordinates.docx");
```

