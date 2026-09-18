---
title: "Aspose::Words::BorderCollection::get_Horizontal Methode"
linktitle: "get_Horizontal"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::get_Horizontal Methode. Gibt den horizontalen Rahmen zurück, der zwischen Zellen oder zusammengehörigen Absätzen in C++ verwendet wird."
type: docs
weight: 8000
url: /de/cpp/aspose.words/bordercollection/get_horizontal/
---
## BorderCollection::get_Horizontal method


Liefert den horizontalen Rahmen, der zwischen Zellen oder passenden Absätzen verwendet wird.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Horizontal()
```


## Beispiele



Zeigt, wie Einstellungen für horizontale Rahmen auf das Format eines Absatzes angewendet werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie einen roten horizontalen Rahmen für den Absatz. Alle anschließend erstellten Absätze erben diese Rahmeneinstellungen.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
borders->get_Horizontal()->set_LineWidth(3);

// Schreiben Sie Text in das Dokument, ohne anschließend einen neuen Absatz zu erstellen.
// Da kein Absatz darunter liegt, wird der horizontale Rahmen nicht sichtbar sein.
builder->Write(u"Paragraph above horizontal border.");

// Sobald wir einen zweiten Absatz hinzufügen, wird der Rahmen des ersten Absatzes sichtbar werden.
builder->InsertParagraph();
builder->Write(u"Paragraph below horizontal border.");

doc->Save(get_ArtifactsDir() + u"Border.HorizontalBorders.docx");
```


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
