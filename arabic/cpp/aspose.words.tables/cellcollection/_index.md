---
title: "Aspose::Words::Tables::CellCollection فئة"
linktitle: "CellCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::CellCollection فئة. يوفر وصولًا مكتوبًا إلى مجموعة من عقد Cell. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.tables/cellcollection/
---
## CellCollection class


يوفر وصولًا مكتوبًا إلى مجموعة من عقد [Cell](../cell/) . لمعرفة المزيد، زر مقالة الوثائق [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class CellCollection : public Aspose::Words::NodeCollection
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | يحصل على عدد العقد في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | يوفر تكرارًا بسيطًا بنمط "foreach" على مجموعة العقد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يسترجع [Cell](../cell/) عند الفهرس المحدد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | يدرج عقدة في المجموعة عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](./toarray/)() | ينسخ جميع الخلايا من المجموعة إلى مصفوفة جديدة من الخلايا. |
| static [Type](./type/)() |  |

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

## انظر أيضًا

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
