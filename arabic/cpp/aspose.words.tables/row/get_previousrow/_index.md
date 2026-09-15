---
title: "طريقة Aspose::Words::Tables::Row::get_PreviousRow"
linktitle: "get_PreviousRow"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Row::get_PreviousRow. يحصل على عقدة الصف السابقة في C++."
type: docs
weight: 11500
url: /ar/cpp/aspose.words.tables/row/get_previousrow/
---
## Row::get_PreviousRow method


يحصل على عقدة [Row](../) السابقة.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Row::get_PreviousRow()
```


## أمثلة



يوضح كيفية تعداد جميع خلايا الجدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// تعداد جميع خلايا الجدول.
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```

## انظر أيضًا

* Class [Row](../)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
