---
title: get_BackgroundShape
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the background shape of the document. Can be null.
type: docs
weight: 14
url: /cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


Gets or sets the background shape of the document. Can be **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## Remarks


Microsoft Word allows only a shape that has its [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) property equal to [Rectangle](../../../aspose.words.drawing/shapetype/) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) to **true**.

## Examples



Shows how to set a background shape for every page of a document. 
```cpp
auto doc = MakeObject<Document>();

ASSERT_TRUE(doc->get_BackgroundShape() == nullptr);

// The only shape type that we can use as a background is a rectangle.
auto shapeRectangle = MakeObject<Shape>(doc, ShapeType::Rectangle);

// There are two ways of using this shape as a page background.
// 1 -  A flat color:
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(ArtifactsDir + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  An image:
shapeRectangle = MakeObject<Shape>(doc, ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(ImageDir + u"Transparent background logo.png");

// Adjust the image's appearance to make it more suitable as a watermark.
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

// Microsoft Word does not support shapes with images as backgrounds,
// but we can still see these backgrounds in other save formats such as .pdf.
doc->Save(ArtifactsDir + u"DocumentBase.BackgroundShape.Image.pdf");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
