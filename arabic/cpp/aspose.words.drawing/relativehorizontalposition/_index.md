---
title: "Aspose::Words::Drawing::RelativeHorizontalPosition enum"
linktitle: "RelativeHorizontalPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::RelativeHorizontalPosition enum. يحدد إلى ما تُعَدُّ الموضعية الأفقية لشكل أو إطار نص في C++."
type: docs
weight: 33000
url: /ar/cpp/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enum


يحدد إلى ماذا يكون موضع الشكل أو إطار النص الأفقي نسبياً.

```cpp
enum class RelativeHorizontalPosition
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| الهامش | 0 | يحدد أن الموضعية الأفقية يجب أن تكون نسبية إلى هوامش الصفحة. |
| Page | 1 | الكائن موضعه نسبياً إلى الحافة اليسرى للصفحة. |
| عمود | 2 | الكائن موضعه نسبياً إلى الجانب الأيسر للعمود. |
| Character | 3 | الكائن موضعه نسبياً إلى الجانب الأيسر للفقرة. |
| LeftMargin | 4 | يحدد أن الموضعية الأفقية يجب أن تكون نسبية إلى الهامش الأيسر للصفحة. |
| RightMargin | 5 | يحدد أن الموضعية الأفقية يجب أن تكون نسبية إلى الهامش الأيمن للصفحة. |
| InsideMargin | 6 | يحدد أن الموضعية الأفقية يجب أن تكون نسبية إلى الهامش الداخلي للصفحة الحالية (الهامش الأيسر في الصفحات الفردية، الأيمن في الصفحات الزوجية). |
| OutsideMargin | 7 | يحدد أن الموضعية الأفقية يجب أن تكون نسبية إلى الهامش الخارجي للصفحة الحالية (الهامش الأيمن في الصفحات الفردية، الأيسر في الصفحات الزوجية). |
| Default | n/a | القيمة الافتراضية هي [Column](./). |


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
