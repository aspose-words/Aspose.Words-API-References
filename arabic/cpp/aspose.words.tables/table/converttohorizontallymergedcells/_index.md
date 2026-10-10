---
title: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells طريقة"
linktitle: "ConvertToHorizontallyMergedCells"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells طريقة. يحول الخلايا المدمجة أفقيًا حسب العرض إلى خلايا مدمجة باستخدام HorizontalMerge في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


يحول الخلايا المدمجة أفقيًا حسب العرض إلى خلايا مدمجة باستخدام [HorizontalMerge](../../cellformat/get_horizontalmerge/).

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## ملاحظات


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

عندما يتم دمج خلية الجدول بواسطة خاصية العرض، يصبح [HorizontalMerge](../../cellformat/get_horizontalmerge/) غير ذي معنى ولكن في بعض الأحيان يكون وجود أعلام الدمج طريقة أكثر ملاءمة.

استخدم هذه الطريقة لتحويل خلايا الجدول المدمجة أفقيًا حسب العرض إلى خلايا مدمجة باستخدام أعلام الدمج.

## أمثلة



يوضح كيفية تحويل الخلايا المدمجة أفقيًا حسب العرض إلى خلايا مدمجة باستخدام CellFormat.HorizontalMerge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table with merged cells.docx");

// لم يعد Microsoft Word يكتب أعلام الدمج، بل يحدد الخلايا المدمجة حسب العرض بدلاً من ذلك.
// تحدد Aspose.Words افتراضيًا 5 خلايا فقط في الصف، ولا تحتوي أي منها على علم الدمج الأفقي،
// على الرغم من وجود 7 خلايا في الصف قبل حدوث الدمج الأفقي.
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
ASSERT_TRUE(row->get_Cells()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> c)>>([](System::SharedPtr<Aspose::Words::Node> c) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Tables::Cell>(c))->get_CellFormat()->get_HorizontalMerge() == Aspose::Words::Tables::CellMerge::None;
}))));

// استخدم طريقة "ConvertToHorizontallyMergedCells" لتحويل الخلايا المدمجة أفقياً
// حسب عرضها إلى الخلية المدمجة أفقياً بواسطة العلامات.
// الآن، لدينا 7 خلايا، وبعضها يحتوي على قيم دمج أفقية.
table->ConvertToHorizontallyMergedCells();
row = table->get_Rows()->idx_get(0);

ASSERT_EQ(7, row->get_Cells()->get_Count());

ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(0)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::First, row->get_Cells()->idx_get(1)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::Previous, row->get_Cells()->idx_get(2)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(3)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::First, row->get_Cells()->idx_get(4)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::Previous, row->get_Cells()->idx_get(5)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(6)->get_CellFormat()->get_HorizontalMerge());
```

## انظر أيضًا

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
