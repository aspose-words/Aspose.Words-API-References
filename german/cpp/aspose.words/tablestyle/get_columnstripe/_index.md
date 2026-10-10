---
title: "Aspose::Words::TableStyle::get_ColumnStripe Methode"
linktitle: "get_ColumnStripe"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TableStyle::get_ColumnStripe Methode. Gibt die Anzahl der Spalten zurück oder legt sie fest, die in die Bandierung einbezogen werden sollen, wenn der Stil ungerade/gerade Spaltenbandierung in C++ angibt."
type: docs
weight: 8000
url: /de/cpp/aspose.words/tablestyle/get_columnstripe/
---
## TableStyle::get_ColumnStripe method


Ruft ab oder legt die Anzahl der Spalten fest, die beim Banden berücksichtigt werden, wenn der Stil ungerade/gerade Spaltenbänderung angibt.

```cpp
int32_t Aspose::Words::TableStyle::get_ColumnStripe()
```


## Beispiele



Zeigt, wie man bedingte Tabellenstile erstellt, die zwischen Zeilen abwechseln.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wir können einen bedingten Stil einer Tabelle konfigurieren, um eine andere Farbe auf die Zeile/Spalte anzuwenden,
// basierend darauf, ob die Zeile/Spalte gerade oder ungerade ist, und ein wechselndes Farb­muster erzeugt.
// Wir können außerdem eine Zahl n auf die Zeilen-/Spalten-Bandbildung anwenden,
// was bedeutet, dass die Farbe nach jeweils n Zeilen/Spalten anstatt nach einer wechselt.
// Erstelle eine Tabelle, bei der einzelne Spalten und Zeilen in Dreiergruppen banded werden.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
for (int32_t i = 0; i < 15; i++)
{
    for (int32_t j = 0; j < 4; j++)
    {
        builder->InsertCell();
        builder->Writeln(System::String::Format(u"{0} column.", (j % 2 == 0 ? System::String(u"Even") : System::String(u"Odd"))));
        builder->Write(System::String::Format(u"Row banding {0}.", (i % 3 == 0 ? System::String(u"start") : System::String(u"continuation"))));
    }
    builder->EndRow();
}
builder->EndTable();

// Wende einen Linienstil auf alle Rahmen der Tabelle an.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// Lege die beiden Farben fest, die sich alle 3 Zeilen abwechseln.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// Legen Sie eine Farbe fest, die auf jede gerade Spalte angewendet wird und jede benutzerdefinierte Zeilenfärbung überschreibt.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// Die "StyleOptions"-Eigenschaft aktiviert standardmäßig die Zeilenbandierung.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Verwenden Sie die "StyleOptions"-Eigenschaft ebenfalls, um die Spaltenbandierung zu aktivieren.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## Siehe auch

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
