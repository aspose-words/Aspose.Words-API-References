---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell"
linktitle: "get_IsLayoutInCell"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell. يحصل على أو يضبط علامة تشير إلى ما إذا كان الشكل يُعرض داخل جدول أو خارجه في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words.drawing/shapebase/get_islayoutincell/
---
## ShapeBase::get_IsLayoutInCell method


الحصول أو تعيين علامة تشير إلى ما إذا كان الشكل معروضًا داخل جدول أو خارجه.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell()
```

## ملاحظات


القيمة الافتراضية هي **true**.

يؤثر فقط على الأشكال ذات المستوى الأعلى، الخاصية [WrapType](../get_wraptype/) التي تم تعيينها إلى قيمة غير [Inline](../../../aspose.words/inline/).

## أمثلة



يوضح كيفية تحديد طريقة عرض الشكل داخل خلية جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(10);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table->set_Style(tableStyle);

builder->MoveTo(table->get_FirstRow()->get_FirstCell()->get_FirstParagraph());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);

// قم بتعيين الخاصية "IsLayoutInCell" إلى "true" لعرض الشكل كعنصر مضمن داخل فقرة الخلية.
// نقطة الأصل الإحداثية التي ستحدد موقع الشكل ستكون الزاوية العلوية اليسرى لخلية الشكل.
// إذا قمنا بتغيير حجم الخلية، سيتحرك الشكل للحفاظ على نفس الموقع بدءًا من الزاوية العلوية اليسرى للخلية.
// قم بتعيين الخاصية "IsLayoutInCell" إلى "false" لعرض الشكل كشكل عائم مستقل.
// نقطة الأصل الإحداثية التي ستحدد موقع الشكل ستكون الزاوية العلوية اليسرى للصفحة،
// ولن يستجيب الشكل لأي تغيير حجم لخليةه.
shape->set_IsLayoutInCell(isLayoutInCell);

// يمكننا تطبيق الخاصية "IsLayoutInCell" فقط على الأشكال العائمة.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

doc->Save(get_ArtifactsDir() + u"Shape.LayoutInTableCell.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
