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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Logo.jpg");
shape->set_WrapType(WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(HorizontalAlignment::Center);
shape->set_VerticalAlignment(VerticalAlignment::Center);

doc->Save(ArtifactsDir + u"Image.CreateFloatingPageCenter.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
