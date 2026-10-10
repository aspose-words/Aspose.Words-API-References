---
title: "Aspose::Words::Tables::PreferredWidth::get_Type metod"
linktitle: "get_Type"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::PreferredWidth::get_Type metod. Hämtar enheten som används för detta föredragna breddvärde i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.tables/preferredwidth/get_type/
---
## PreferredWidth::get_Type method


Hämtar måttenheten som används för detta föredragna breddvärde.

```cpp
Aspose::Words::Tables::PreferredWidthType Aspose::Words::Tables::PreferredWidth::get_Type() const
```


## Exempel



Visar hur man verifierar den föredragna breddtypen och värdet för en tabellcell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Se även

* Enum [PreferredWidthType](../../preferredwidthtype/)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
