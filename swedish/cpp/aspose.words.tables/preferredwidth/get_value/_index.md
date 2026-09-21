---
title: "Aspose::Words::Tables::PreferredWidth::get_Value metod"
linktitle: "get_Value"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::PreferredWidth::get_Value metod. Hämtar det föredragna breddvärdet. Enheten specificeras i egenskapen Type i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


Hämtar det föredragna breddvärdet. Enheten specificeras i egenskapen [Type](../get_type/).

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
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

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
