---
title: "طريقة Aspose::Words::PageSetup::get_LeftMargin"
linktitle: "get_LeftMargin"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_LeftMargin. تُرجِع أو تُعيّن المسافة (بالنقاط) بين الحافة اليسرى للصفحة والحد الأيسر للنص الأساسي في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words/pagesetup/get_leftmargin/
---
## PageSetup::get_LeftMargin method


يعيد أو يعيّن المسافة (بالنقاط) بين الحافة اليسرى للصفحة والحد الأيسر للنص الأساسي.

```cpp
double Aspose::Words::PageSetup::get_LeftMargin()
```


## أمثلة



يظهر كيفية تعديل حجم الورق، الاتجاه، الهوامش، بالإضافة إلى إعدادات أخرى لقسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
