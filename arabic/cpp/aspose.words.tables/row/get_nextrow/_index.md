---
title: "طريقة Aspose::Words::Tables::Row::get_NextRow"
linktitle: "get_NextRow"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Row::get_NextRow. يحصل على عقدة الصف التالية في C++."
type: docs
weight: 9500
url: /ar/cpp/aspose.words.tables/row/get_nextrow/
---
## Row::get_NextRow method


يحصل على عقدة [Row](../) التالية.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Row::get_NextRow()
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
