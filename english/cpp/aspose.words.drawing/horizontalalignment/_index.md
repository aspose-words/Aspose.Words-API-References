---
title: Aspose::Words::Drawing::HorizontalAlignment enum
linktitle: HorizontalAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::HorizontalAlignment enum. Specifies horizontal alignment of a floating shape, text frame or floating table in C++.'
type: docs
weight: 26000
url: /cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


Specifies horizontal alignment of a floating shape, text frame or floating table.

```cpp
enum class HorizontalAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | The object is explicitly positioned, usually using its **Left** property. |
| Default | n/a | Same as [None](./). |
| Left | 1 | Specifies that the object shall be left aligned to the horizontal alignment base. |
| Center | 2 | Specifies that the object shall be centered with respect to the horizontal alignment base. |
| Right | 3 | Specifies that the object shall be right aligned to the horizontal alignment base. |
| Inside | 4 | Specifies that the object shall be inside of the horizontal alignment base. |
| Outside | 5 | Specifies that the object shall be outside of the horizontal alignment base. |


## Examples



Shows how to insert a floating image to the center of a page. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
