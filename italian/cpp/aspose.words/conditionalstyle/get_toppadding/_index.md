---
title: "Metodo Aspose::Words::ConditionalStyle::get_TopPadding"
linktitle: "get_TopPadding"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ConditionalStyle::get_TopPadding. Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle della tabella in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/conditionalstyle/get_toppadding/
---
## ConditionalStyle::get_TopPadding method


Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle della tabella.

```cpp
double Aspose::Words::ConditionalStyle::get_TopPadding()
```


## Esempi



Mostra come lavorare con alcuni stili di area di una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Cell 3");
builder->InsertCell();
builder->Write(u"Cell 4");
builder->EndTable();

// Crea uno stile di tabella personalizzato.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));

// Gli stili condizionali sono modifiche di formattazione che influenzano solo alcune celle della tabella.
// basati su un predicato, ad esempio le celle che si trovano nell'ultima riga.
// Di seguito sono riportati tre modi per accedere agli stili condizionali di uno stile di tabella dalla collezione "ConditionalStyles".
// 1 -  Per tipo di stile:
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::FirstRow)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  Per indice:
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
ASSERT_EQ(Aspose::Words::ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  Come proprietà:
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// Applica spaziatura e formattazione del testo agli stili condizionali.
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// Elenca tutte le possibili condizioni di stile.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::ConditionalStyle>>> enumerator = tableStyle->get_ConditionalStyles()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::ConditionalStyle> currentStyle = enumerator->get_Current();
        if (currentStyle != nullptr)
        {
            std::cout << System::EnumGetName(currentStyle->get_Type()) << std::endl;
        }
    }
}

// Applica lo stile personalizzato, che contiene tutti gli stili condizionali, alla tabella.
table->set_Style(tableStyle);

// Il nostro stile applica alcuni stili condizionali per impostazione predefinita.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Dovremo abilitare tutti gli altri stili noi stessi tramite la proprietà "StyleOptions".
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::LastRow | Aspose::Words::Tables::TableStyleOptions::LastColumn);

doc->Save(get_ArtifactsDir() + u"Table.ConditionalStyles.docx");
```

## Vedi anche

* Class [ConditionalStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
