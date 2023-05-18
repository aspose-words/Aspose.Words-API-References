---
title: Aspose::Words::Drawing::ShapeBase::get_HRef method
linktitle: get_HRef
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_HRef method. Gets or sets the full hyperlink address for a shape in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words.drawing/shapebase/get_href/
---
## ShapeBase::get_HRef method


Gets or sets the full hyperlink address for a shape.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_HRef()
```

## Remarks


The default value is an empty string.

Below are examples of valid values for this property:

Full URI: **https://www.aspose.com/**.

Full file name: **C:\\My Documents\\SalesReport.doc**.

Relative URI: **%../../../resource.txt**

Relative file name: **%..\\My Documents\\SalesReport.doc**.

[Bookmark](../../../aspose.words/bookmark/) within another document: **https://www.aspose.com/Products/Default.aspx::Suites**

[Bookmark](../../../aspose.words/bookmark/) within this document: **%#BookmakName**.

## Examples



Shows how to insert a shape which contains an image, and is also a hyperlink. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
// and take us to the hyperlink in the "HRef" property.
doc->Save(ArtifactsDir + u"Image.InsertImageWithHyperlink.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
