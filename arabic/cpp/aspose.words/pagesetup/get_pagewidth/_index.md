---
title: "طريقة Aspose::Words::PageSetup::get_PageWidth"
linktitle: "get_PageWidth"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageSetup::get_PageWidth method. تُرجع أو تُعيّن عرض الصفحة بالنقاط في C++."
type: docs
weight: 36000
url: /ar/cpp/aspose.words/pagesetup/get_pagewidth/
---
## PageSetup::get_PageWidth method


إرجاع أو تعيين عرض الصفحة بالنقاط.

```cpp
double Aspose::Words::PageSetup::get_PageWidth()
```


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


يُظهر كيفية إدراج صورة عائمة، وتحديد موضعها وحجمها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// قم بتكوين خاصية "RelativeHorizontalPosition" للشكل لتعامل مع قيمة خاصية "Left"
// كالمسافة الأفقية للشكل، بالنقاط، من الجانب الأيسر للصفحة.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// عيّن المسافة الأفقية للشكل من الجانب الأيسر للصفحة إلى 100.
shape->set_Left(100);

// استخدم خاصية "RelativeVerticalPosition" بطريقة مماثلة لتحديد موضع الشكل 80 نقطة أسفل أعلى الصفحة.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// عيّن ارتفاع الشكل، والذي سيُعيد تحجيم العرض تلقائيًا للحفاظ على الأبعاد.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// خاصيتي "Bottom" و "Right" تحتويان على الحافة السفلية واليمنى للصورة.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
