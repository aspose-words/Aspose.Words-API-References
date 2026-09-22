---
title: "طريقة Aspose::Words::PageSetup::get_PageHeight"
linktitle: "get_PageHeight"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_PageHeight. تُرجع أو تعيّن ارتفاع الصفحة بالنقاط في C++."
type: docs
weight: 33000
url: /ar/cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


يعيد أو يعيّن ارتفاع الصفحة بالنقاط.

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
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

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
