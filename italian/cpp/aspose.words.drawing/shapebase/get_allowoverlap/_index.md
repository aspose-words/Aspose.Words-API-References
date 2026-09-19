---
title: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap metodo"
linktitle: "get_AllowOverlap"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap metodo. Ottiene o imposta un valore che specifica se questa forma può sovrapporsi ad altre forme in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase::get_AllowOverlap method


Ottiene o imposta un valore che specifica se questa forma può sovrapporsi ad altre forme.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```

## Note


Questa proprietà influisce sul comportamento della forma in Microsoft Word. Aspose.Words ignora il valore di questa proprietà.

Questa proprietà è applicabile solo alle forme di livello superiore.

Il valore predefinito è **true**.

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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
