---
title: "Classe Aspose::Words::ConditionalStyleCollection"
linktitle: "ConditionalStyleCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::ConditionalStyleCollection. Rappresenta una raccolta di oggetti ConditionalStyle. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


Rappresenta una raccolta di oggetti [ConditionalStyle](../conditionalstyle/). Per saperne di più, visita l'articolo della documentazione [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Cancella tutti gli stili condizionali dello stile di tabella. |
| [get_BottomLeftCell](./get_bottomleftcell/)() | Ottiene lo stile della cella in basso a sinistra. |
| [get_BottomRightCell](./get_bottomrightcell/)() | Ottiene lo stile della cella in basso a destra. |
| [get_Count](./get_count/)() const | Ottiene il numero di stili condizionali nella raccolta. |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | Ottiene lo stile di bande delle colonne pari. |
| [get_EvenRowBanding](./get_evenrowbanding/)() | Ottiene lo stile di bande delle righe pari. |
| [get_FirstColumn](./get_firstcolumn/)() | Ottiene lo stile della prima colonna. |
| [get_FirstRow](./get_firstrow/)() | Ottiene lo stile della prima riga. |
| [get_LastColumn](./get_lastcolumn/)() | Ottiene lo stile dell'ultima colonna. |
| [get_LastRow](./get_lastrow/)() | Ottiene lo stile dell'ultima riga. |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | Ottiene lo stile di bande delle colonne dispari. |
| [get_OddRowBanding](./get_oddrowbanding/)() | Ottiene lo stile di bande delle righe dispari. |
| [get_TopLeftCell](./get_topleftcell/)() | Ottiene lo stile della cella in alto a sinistra. |
| [get_TopRightCell](./get_toprightcell/)() | Ottiene lo stile della cella in alto a destra. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli stili condizionali nella collezione. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | Recupera un oggetto [ConditionalStyle](../conditionalstyle/) per tipo di stile condizionale. |
| [idx_get](./idx_get/)(int32_t) | Recupera un oggetto [ConditionalStyle](../conditionalstyle/) per indice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
