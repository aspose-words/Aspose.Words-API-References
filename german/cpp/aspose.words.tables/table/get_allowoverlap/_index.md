---
title: "Aspose::Words::Tables::Table::get_AllowOverlap-Methode"
linktitle: "get_AllowOverlap"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_AllowOverlap-Methode. Ermittelt, ob eine schwebende Tabelle anderen schwebenden Objekten im Dokument erlaubt, ihre Ausmaße bei der Anzeige zu überlappen. Der Standardwert ist true in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words.tables/table/get_allowoverlap/
---
## Table::get_AllowOverlap method


Liest, ob eine schwebende Tabelle anderen schwebenden Objekten im Dokument erlaubt, ihre Ausmaße bei der Anzeige zu überlappen. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::Tables::Table::get_AllowOverlap()
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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
