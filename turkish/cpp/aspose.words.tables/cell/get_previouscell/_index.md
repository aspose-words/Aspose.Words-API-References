---
title: "Aspose::Words::Tables::Cell::get_PreviousCell yöntemi"
linktitle: "get_PreviousCell"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Cell::get_PreviousCell yöntemi. C++'de önceki Cell düğümünü alır."
type: docs
weight: 12500
url: /tr/cpp/aspose.words.tables/cell/get_previouscell/
---
## Cell::get_PreviousCell method


Önceki [Cell](../) düğümünü alır.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_PreviousCell()
```


## Örnekler



Tüm tablo hücrelerinde nasıl yineleme yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Tablonun tüm hücrelerinde yineleme yap.
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```

## Ayrıca Bakınız

* Class [Cell](../)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
