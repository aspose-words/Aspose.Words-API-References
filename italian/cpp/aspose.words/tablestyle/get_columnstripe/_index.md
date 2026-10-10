---
title: "Aspose::Words::TableStyle::get_ColumnStripe method"
linktitle: "get_ColumnStripe"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TableStyle::get_ColumnStripe method. Ottiene o imposta un numero di colonne da includere nella striscia quando lo stile specifica la striscia di colonne pari/dispari in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/tablestyle/get_columnstripe/
---
## TableStyle::get_ColumnStripe method


Ottiene o imposta un numero di colonne da includere nella striscia quando lo stile specifica la striscia di colonne dispari/pari.

```cpp
int32_t Aspose::Words::TableStyle::get_ColumnStripe()
```


## Esempi



Mostra come creare stili di tabella condizionali che alternano le righe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Possiamo configurare uno stile condizionale di una tabella per applicare un colore diverso alla riga/colonna,
// in base al fatto che la riga/colonna sia pari o dispari, creando un modello di colore alternato.
// Possiamo anche applicare un numero n alla striscia di righe/colonne,
// significando che il colore alterna dopo ogni n righe/colonne invece di una.
// Crea una tabella in cui le singole colonne e righe saranno raggruppate, le colonne saranno raggruppate a gruppi di tre.
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

// Applica uno stile di linea a tutti i bordi della tabella.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// Imposta i due colori, che si alterneranno ogni 3 righe.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// Imposta un colore da applicare a ogni colonna pari, che sovrascriverà qualsiasi colorazione personalizzata delle righe.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// La proprietà "StyleOptions" abilita la striscia di righe per impostazione predefinita.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Usa anche la proprietà "StyleOptions" per abilitare la striscia di colonne.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## Vedi anche

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
