---
title: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter طريقة"
linktitle: "MoveToHeaderFooter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter طريقة. ينقل المؤشر إلى بداية رأس أو تذييل في القسم الحالي في C++."
type: docs
weight: 57000
url: /ar/cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


ينقل المؤشر إلى بداية رأس أو تذييل في القسم الحالي.

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | يحدد الرأس أو التذييل الذي سيتم الانتقال إليه. |
## ملاحظات


بعد أن نقلت المؤشر إلى رأس أو تذييل، يمكنك استخدام باقي طرق [DocumentBuilder](../) لتعديل محتويات الرأس أو التذييل.

إذا كنت تريد إنشاء رؤوس وتذييلات مختلفة للصفحة الأولى، تحتاج إلى ضبط [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/).

إذا كنت تريد إنشاء رؤوس وتذييلات مختلفة للصفحات الزوجية والفردية، تحتاج إلى ضبط [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/).

استخدم [MoveToSection()](../movetosection/) للخروج من الرأس إلى النص الرئيسي.

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

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
