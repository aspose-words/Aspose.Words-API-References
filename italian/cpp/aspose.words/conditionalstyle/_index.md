---
title: "Aspose::Words::ConditionalStyle class"
linktitle: "ConditionalStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::ConditionalStyle. Rappresenta una formattazione speciale applicata a una certa area di una tabella con lo stile di tabella assegnato. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words/conditionalstyle/
---
## ConditionalStyle class


Rappresenta una formattazione speciale applicata a un'area di una tabella con lo stile di tabella assegnato. Per saperne di più, visita l'articolo di documentazione [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyle : public Aspose::Words::IBorderAttrSource,
                         public Aspose::Words::IShadingAttrSource,
                         public Aspose::Words::IParaAttrSource,
                         public Aspose::Words::IRunAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Cancella la formattazione di questo stile condizionale. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Confronta questo stile condizionale con l'oggetto specificato. |
| [get_Borders](./get_borders/)() | Ottiene la raccolta dei bordi di cella predefiniti per lo stile condizionale. |
| [get_BottomPadding](./get_bottompadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto delle celle della tabella. |
| [get_Font](./get_font/)() | Ottiene la formattazione dei caratteri dello stile condizionale. |
| [get_LeftPadding](./get_leftpadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle della tabella. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Ottiene la formattazione del paragrafo dello stile condizionale. |
| [get_RightPadding](./get_rightpadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle della tabella. |
| [get_Shading](./get_shading/)() | Ottiene un oggetto [Shading](../shading/) che si riferisce alla formattazione dell'ombreggiatura per questo stile condizionale. |
| [get_TopPadding](./get_toppadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle della tabella. |
| [get_Type](./get_type/)() | Ottiene l'area della tabella a cui si riferisce questo stile condizionale. |
| [GetHashCode](./gethashcode/)() const override | Calcola il codice hash per questo oggetto. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Metodo impostatore per [Aspose::Words::ConditionalStyle::get_BottomPadding](./get_bottompadding/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Metodo impostatore per [Aspose::Words::ConditionalStyle::get_LeftPadding](./get_leftpadding/). |
| [set_RightPadding](./set_rightpadding/)(double) | Metodo impostatore per [Aspose::Words::ConditionalStyle::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Metodo impostatore per [Aspose::Words::ConditionalStyle::get_TopPadding](./get_toppadding/). |
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
