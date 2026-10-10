---
title: "Aspose::Words::Tables::Table::get_HorizontalAnchor metodo"
linktitle: "get_HorizontalAnchor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_HorizontalAnchor metodo. Ottiene l'oggetto base da cui deve essere calcolata la posizione orizzontale della tabella fluttuante. Il valore predefinito è Column in C++."
type: docs
weight: 24000
url: /it/cpp/aspose.words.tables/table/get_horizontalanchor/
---
## Table::get_HorizontalAnchor method


Ottiene l'oggetto base da cui deve essere calcolata la posizione orizzontale della tabella fluttuante. Il valore predefinito è [Column](../../../aspose.words.drawing/relativehorizontalposition/).

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Tables::Table::get_HorizontalAnchor()
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

* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
