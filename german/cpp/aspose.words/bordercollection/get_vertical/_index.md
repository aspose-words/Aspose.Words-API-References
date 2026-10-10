---
title: "Aspose::Words::BorderCollection::get_Vertical Methode"
linktitle: "get_Vertical"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::get_Vertical Methode. Gibt den vertikalen Rahmen zurück, der zwischen Zellen in C++ verwendet wird."
type: docs
weight: 15000
url: /de/cpp/aspose.words/bordercollection/get_vertical/
---
## BorderCollection::get_Vertical method


Liefert den vertikalen Rahmen, der zwischen Zellen verwendet wird.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Vertical()
```


## Beispiele



Zeigt, wie Einstellungen für vertikale Rahmen auf das Format einer Tabellenzeile angewendet werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie eine Tabelle mit roten und blauen inneren Rahmen.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

for (int32_t i = 0; i < 3; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 1", i + 1));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 2", i + 1));

    System::SharedPtr<Aspose::Words::Tables::Row> row = builder->EndRow();
    System::SharedPtr<Aspose::Words::BorderCollection> borders = row->get_RowFormat()->get_Borders();

    // Passen Sie das Aussehen der Rahmen an, die zwischen Zeilen erscheinen.
    borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
    borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Horizontal()->set_LineWidth(2.0);

    // Passen Sie das Aussehen der Rahmen an, die zwischen Zellen erscheinen.
    borders->get_Vertical()->set_Color(System::Drawing::Color::get_Blue());
    borders->get_Vertical()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Vertical()->set_LineWidth(2.0);
}

// Ein Zeilenformat und ein innerer Absatz einer Zelle verwenden unterschiedliche Rahmeneinstellungen.
System::SharedPtr<Aspose::Words::Border> border = table->get_FirstRow()->get_FirstCell()->get_LastParagraph()->get_ParagraphFormat()->get_Borders()->get_Vertical();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());

doc->Save(get_ArtifactsDir() + u"Border.VerticalBorders.docx");
```

## Siehe auch

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
