---
title: get_GradientStops
second_title: Aspose.Words for C++ API Reference
description: Gets a collection of GradientStop objects for the fill.
type: docs
weight: 79
url: /cpp/aspose.words.drawing/fill/get_gradientstops/
---
## Fill::get_GradientStops method


Gets a collection of [GradientStop](../../gradientstop/) objects for the fill.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GradientStopCollection> Aspose::Words::Drawing::Fill::get_GradientStops()
```


## Examples



Shows how to add gradient stops to the gradient fill. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Rectangle, 80, 80);
shape->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Green(), System::Drawing::Color::get_Red(), GradientStyle::Horizontal,
                                    GradientVariant::Variant2);

// Get gradient stops collection.
SharedPtr<GradientStopCollection> gradientStops = shape->get_Fill()->get_GradientStops();

// Change first gradient stop.
gradientStops->idx_get(0)->set_Color(System::Drawing::Color::get_Aqua());
gradientStops->idx_get(0)->set_Position(0.1);
gradientStops->idx_get(0)->set_Transparency(0.25);

// Add new gradient stop to the end of collection.
auto gradientStop = MakeObject<GradientStop>(System::Drawing::Color::get_Brown(), 0.5);
gradientStops->Add(gradientStop);

// Remove gradient stop at index 1.
gradientStops->RemoveAt(1);
// And insert new gradient stop at the same index 1.
gradientStops->Insert(1, MakeObject<GradientStop>(System::Drawing::Color::get_Chocolate(), 0.75, 0.3));

// Remove last gradient stop in the collection.
gradientStop = gradientStops->idx_get(2);
gradientStops->Remove(gradientStop);

ASSERT_EQ(2, gradientStops->get_Count());

ASSERT_EQ(System::Drawing::Color::get_Aqua().ToArgb(), gradientStops->idx_get(0)->get_Color().ToArgb());
ASSERT_NEAR(0.1, gradientStops->idx_get(0)->get_Position(), 0.01);
ASSERT_NEAR(0.25, gradientStops->idx_get(0)->get_Transparency(), 0.01);

ASSERT_EQ(System::Drawing::Color::get_Chocolate().ToArgb(), gradientStops->idx_get(1)->get_Color().ToArgb());
ASSERT_NEAR(0.75, gradientStops->idx_get(1)->get_Position(), 0.01);
ASSERT_NEAR(0.3, gradientStops->idx_get(1)->get_Transparency(), 0.01);

// Use the compliance option to define the shape using DML
// if you want to get "GradientStops" property after the document saves.
auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(ArtifactsDir + u"Shape.GradientStops.docx", saveOptions);
```

## See Also

* Class [GradientStopCollection](../../gradientstopcollection/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
