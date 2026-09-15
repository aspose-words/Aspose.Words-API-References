---
title: "Aspose::Words::Drawing::RelativeVerticalPosition enum"
linktitle: "RelativeVerticalPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::RelativeVerticalPosition enum. يحدد إلى ماذا يكون الموضع الرأسي لشكل أو إطار نصي نسبياً في C++."
type: docs
weight: 34000
url: /ar/cpp/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enum


يحدد إلى ماذا يكون موضع الشكل أو إطار النص العمودي نسبياً.

```cpp
enum class RelativeVerticalPosition
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| الهامش | 0 | يحدد أن التحديد الرأسي يجب أن يكون نسبياً إلى هوامش الصفحة. |
| Page | 1 | الكائن موضعه نسبياً إلى الحافة العلوية للصفحة. |
| Paragraph | 2 | الكائن موضعه نسبياً إلى أعلى الفقرة التي تحتوي على المرساة. |
| خط | 3 | غير موثق. |
| TopMargin | 4 | يحدد أن التحديد الرأسي يجب أن يكون نسبياً إلى الهامش العلوي للصفحة الحالية. |
| BottomMargin | 5 | يحدد أن التحديد الرأسي يجب أن يكون نسبياً إلى الهامش السفلي للصفحة الحالية. |
| InsideMargin | 6 | يحدد أن التحديد الرأسي يجب أن يكون نسبياً إلى الهامش الداخلي للصفحة الحالية. |
| OutsideMargin | 7 | يحدد أن التحديد الرأسي يجب أن يكون نسبياً إلى الهامش الخارجي للصفحة الحالية. |
| TableDefault | n/a | القيمة الافتراضية هي [Margin](./). |
| TextFrameDefault | n/a | القيمة الافتراضية هي [Paragraph](./). |


## أمثلة



يوضح كيفية إدراج صورة واستخدامها كعلامة مائية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج الصورة في الترويسة بحيث تكون مرئية في كل صفحة.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// ضع الصورة في مركز الصفحة.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


يوضح كيفية إدراج صورة عائمة في مركز الصفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج صورة عائمة ستظهر خلف النص المتداخل ووازنها إلى مركز الصفحة.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
