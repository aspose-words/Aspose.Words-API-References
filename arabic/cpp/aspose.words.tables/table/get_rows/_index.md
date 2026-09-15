---
title: "Aspose::Words::Tables::Table::get_Rows طريقة"
linktitle: "get_Rows"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::get_Rows طريقة. يوفر وصولًا من نوع محدد إلى صفوف الجدول في C++."
type: docs
weight: 33000
url: /ar/cpp/aspose.words.tables/table/get_rows/
---
## Table::get_Rows method


يوفر وصولًا مكتوبًا للصفوف في الجدول.

```cpp
System::SharedPtr<Aspose::Words::Tables::RowCollection> Aspose::Words::Tables::Table::get_Rows()
```


## أمثلة



يظهر كيفية التكرار عبر جميع الجداول في المستند وطباعة محتويات كل خلية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // يمكننا استخدام طريقة "ToArray" على مجموعة الصفوف لاستنساخها إلى مصفوفة.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // يمكننا استخدام طريقة "ToArray" على مجموعة الخلايا لاستنساخها إلى مصفوفة.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```


يوضح كيفية دمج الصفوف من جدولين في جدول واحد.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// فيما يلي طريقتان للحصول على جدول من مستند.
// 1 - من مجموعة \"Tables\" لعقدة Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 - باستخدام طريقة \"GetChild\":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// إلحاق جميع الصفوف من الجدول الحالي إلى التالي.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// إزالة حاوية الجدول الفارغة.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## انظر أيضًا

* Class [RowCollection](../../rowcollection/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
