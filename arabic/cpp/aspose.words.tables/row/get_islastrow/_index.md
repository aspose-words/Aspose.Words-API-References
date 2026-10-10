---
title: "Aspose::Words::Tables::Row::get_IsLastRow طريقة"
linktitle: "get_IsLastRow"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Row::get_IsLastRow طريقة. صحيح إذا كان هذا هو الصف الأخير في جدول؛ خطأ خلاف ذلك في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.tables/row/get_islastrow/
---
## Row::get_IsLastRow method


صحيح إذا كان هذا هو الصف الأخير في جدول؛ خطأ خلاف ذلك.

```cpp
bool Aspose::Words::Tables::Row::get_IsLastRow()
```


## أمثلة



يظهر كيفية ضبط جدول للبقاء معًا على نفس الصفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// تمكين KeepWithNext لكل فقرة في الجدول باستثناء
// الأخيرة في الصف الأخير ستمنع الجدول من الانقسام عبر صفحات متعددة.
for (auto&& cell : System::IterateOver<Aspose::Words::Tables::Cell>(table->GetChildNodes(Aspose::Words::NodeType::Cell, true)))
{
    for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(cell->get_Paragraphs()))
    {
        ASSERT_TRUE(para->get_IsInCell());

        if (!(cell->get_ParentRow()->get_IsLastRow() && para->get_IsEndOfCell()))
        {
            para->get_ParagraphFormat()->set_KeepWithNext(true);
        }
    }
}

doc->Save(get_ArtifactsDir() + u"Table.KeepTableTogether.docx");
```

## انظر أيضًا

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
