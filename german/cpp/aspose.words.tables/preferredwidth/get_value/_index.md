---
title: "Aspose::Words::Tables::PreferredWidth::get_Value Methode"
linktitle: "get_Value"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::PreferredWidth::get_Value Methode. Gibt den Wert der bevorzugten Breite zurück. Die Maßeinheit wird in der Type‑Eigenschaft in C++ angegeben."
type: docs
weight: 7000
url: /de/cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


Gibt den Wert der bevorzugten Breite zurück. Die Maßeinheit wird in der [Type](../get_type/) Eigenschaft angegeben.

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
```


## Beispiele



Zeigt, wie der Typ und der Wert der bevorzugten Breite einer Tabellenzelle überprüft werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Siehe auch

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
