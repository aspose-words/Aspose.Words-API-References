---
title: "Aspose::Words::Tables::PreferredWidth::get_Type Methode"
linktitle: "get_Type"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::PreferredWidth::get_Type Methode. Gibt die für diesen bevorzugten Breitenwert in C++ verwendete Maßeinheit zurück."
type: docs
weight: 6000
url: /de/cpp/aspose.words.tables/preferredwidth/get_type/
---
## PreferredWidth::get_Type method


Liefert die für diesen bevorzugten Breitenwert verwendete Maßeinheit.

```cpp
Aspose::Words::Tables::PreferredWidthType Aspose::Words::Tables::PreferredWidth::get_Type() const
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

* Enum [PreferredWidthType](../../preferredwidthtype/)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
