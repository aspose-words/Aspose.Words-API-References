---
title: "Aspose::Words::Tables::Table::get_VerticalAnchor metodo"
linktitle: "get_VerticalAnchor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_VerticalAnchor metodo. Ottiene l'oggetto di base da cui deve essere calcolata la posizione verticale della tabella flottante. Il valore predefinito è Margin in C++."
type: docs
weight: 41000
url: /it/cpp/aspose.words.tables/table/get_verticalanchor/
---
## Table::get_VerticalAnchor method


Ottiene l'oggetto di base da cui deve essere calcolata la posizione verticale della tabella flottante. Il valore predefinito è [Margin](../../../aspose.words.drawing/relativeverticalposition/).

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Tables::Table::get_VerticalAnchor()
```


## Esempi



Mostra come lavorare con le proprietà delle tabelle flottanti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // Solo Margin, Page, Column sono disponibili in RelativeHorizontalPosition per il setter HorizontalAnchor.
    // Verrà sollevata un'ArgumentException per qualsiasi altro valore.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // Solo Margin, Page, Paragraph sono disponibili in RelativeVerticalPosition per il setter VerticalAnchor.
    // Verrà sollevata un'ArgumentException per qualsiasi altro valore.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## Vedi anche

* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
