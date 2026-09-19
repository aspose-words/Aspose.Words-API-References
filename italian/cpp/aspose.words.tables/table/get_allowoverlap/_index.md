---
title: "Aspose::Words::Tables::Table::get_AllowOverlap metodo"
linktitle: "get_AllowOverlap"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_AllowOverlap metodo. Ottiene se una tabella flottante deve consentire ad altri oggetti flottanti nel documento di sovrapporsi ai suoi limiti quando visualizzata. Il valore predefinito è true in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.tables/table/get_allowoverlap/
---
## Table::get_AllowOverlap method


Ottiene se una tabella fluttuante deve consentire ad altri oggetti fluttuanti nel documento di sovrapporsi alle sue dimensioni quando visualizzata. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Tables::Table::get_AllowOverlap()
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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
