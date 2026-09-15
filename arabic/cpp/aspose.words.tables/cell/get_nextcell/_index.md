---
title: "طريقة Aspose::Words::Tables::Cell::get_NextCell"
linktitle: "get_NextCell"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Cell::get_NextCell. يحصل على عقدة Cell التالية في C++."
type: docs
weight: 9500
url: /ar/cpp/aspose.words.tables/cell/get_nextcell/
---
## Cell::get_NextCell method


يحصل على عقدة [Cell](../) التالية.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_NextCell()
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

* Class [Cell](../)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
