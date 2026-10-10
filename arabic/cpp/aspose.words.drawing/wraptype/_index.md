---
title: "عدد Aspose::Words::Drawing::WrapType"
linktitle: "WrapType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "عدد Aspose::Words::Drawing::WrapType. يحدد كيفية لف النص حول شكل أو صورة في C++."
type: docs
weight: 45000
url: /ar/cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


يحدد كيفية التفاف النص حول الشكل أو الصورة.

```cpp
enum class WrapType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 3 | لا يوجد لف للنص حول الشكل. يتم وضع الشكل خلف النص أو أمامه. |
| متضمن | 0 | يبقى الشكل على نفس طبقة النص ويُعامل كحرف. |
| TopBottom | 1 | يتوقف النص عند أعلى الشكل ويستأنف على السطر أسفل الشكل. |
| Square | 2 | يلف النص حول جميع جوانب الصندوق المحدد المربع للشكل. |
| Tight | 4 | يلف بإحكام حول حواف الشكل، بدلاً من اللف حول الصندوق المحدد. |
| Through | 5 | نفس طريقة Tight، لكنه يلف داخل أي أجزاء من الشكل المفتوحة. |


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
