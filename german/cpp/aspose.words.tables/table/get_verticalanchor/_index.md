---
title: "Aspose::Words::Tables::Table::get_VerticalAnchor Methode"
linktitle: "get_VerticalAnchor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_VerticalAnchor Methode. Gibt das Basisobjekt zurück, von dem aus die vertikale Positionierung der schwebenden Tabelle berechnet werden soll. Der Standardwert ist Margin in C++."
type: docs
weight: 41000
url: /de/cpp/aspose.words.tables/table/get_verticalanchor/
---
## Table::get_VerticalAnchor method


Ermittelt das Basisobjekt, von dem aus die vertikale Positionierung der schwebenden Tabelle berechnet werden soll. Der Standardwert ist [Margin](../../../aspose.words.drawing/relativeverticalposition/).

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Tables::Table::get_VerticalAnchor()
```


## Beispiele



Zeigt, wie man mit den Eigenschaften schwebender Tabellen arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // Nur Margin, Page und Column sind in RelativeHorizontalPosition für den HorizontalAnchor-Setter verfügbar.
    // Eine ArgumentException wird für alle anderen Werte ausgelöst.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // Nur Margin, Page und Paragraph sind in RelativeVerticalPosition für den VerticalAnchor-Setter verfügbar.
    // Eine ArgumentException wird für alle anderen Werte ausgelöst.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## Siehe auch

* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
