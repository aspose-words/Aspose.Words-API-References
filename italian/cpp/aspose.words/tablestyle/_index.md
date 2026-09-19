---
title: "Aspose::Words::TableStyle classe"
linktitle: "TableStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TableStyle classe. Rappresenta uno stile di tabella. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 67000
url: /it/cpp/aspose.words/tablestyle/
---
## TableStyle class


Rappresenta uno stile di tabella. Per saperne di più, visita l'articolo di documentazione [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableStyle : public Aspose::Words::Style,
                   public Aspose::Words::ICellAttrSource,
                   public Aspose::Words::IRowAttrSource,
                   public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Equals](../style/equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Confronta con lo stile specificato. Gli Istd degli stili sono confrontati solo per gli stili integrati. I valori predefiniti degli stili non sono inclusi nel confronto. Lo stile base, lo stile collegato e lo stile del paragrafo successivo sono confrontati ricorsivamente. |
| [get_Aliases](../style/get_aliases/)() | Restituisce tutti gli alias di questo stile. Se lo stile non ha alias, viene restituito un array vuoto di stringhe. |
| [get_Alignment](./get_alignment/)() | Specifica l'allineamento per lo stile di tabella. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Ottiene o imposta un flag che indica se il testo in una riga di tabella può essere diviso tra interruzioni di pagina. |
| [get_AutomaticallyUpdate](../style/get_automaticallyupdate/)() const | Specifica se questo stile è ridefinito automaticamente in base al valore appropriato. |
| [get_BaseStyleName](../style/get_basestylename/)() | Ottiene/Imposta il nome dello stile su cui si basa questo stile. |
| [get_Borders](./get_borders/)() | Ottiene la raccolta dei bordi predefiniti delle celle per lo stile. |
| [get_BottomPadding](./get_bottompadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto delle celle della tabella. |
| [get_BuiltIn](../style/get_builtin/)() | Vero se questo stile è uno degli stili integrati in MS Word. |
| [get_CellSpacing](./get_cellspacing/)() | Ottiene o imposta la quantità di spazio (in punti) tra le celle. |
| [get_ColumnStripe](./get_columnstripe/)() | Ottiene o imposta un numero di colonne da includere nella striscia quando lo stile specifica la striscia di colonne dispari/pari. |
| [get_ConditionalStyles](./get_conditionalstyles/)() | Raccolta di stili condizionali che possono essere definiti per questo stile di tabella. |
| [get_Document](../style/get_document/)() | Restituisce il documento proprietario. |
| [get_Font](../style/get_font/)() | Ottiene la formattazione dei caratteri dello stile. |
| [get_IsHeading](../style/get_isheading/)() | Vero quando lo stile è uno degli stili di intestazione integrati. |
| [get_IsQuickStyle](../style/get_isquickstyle/)() const | Specifica se questo stile è mostrato nella galleria Rapida [Style](../style/) all'interno dell'interfaccia di MS Word. |
| [get_LeftIndent](./get_leftindent/)() | Ottiene o imposta il valore che rappresenta l'indentazione sinistra di una tabella. |
| [get_LeftPadding](./get_leftpadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle della tabella. |
| [get_LinkedStyleName](../style/get_linkedstylename/)() | Ottiene/imposta il nome del [Style](../style/) collegato a questo. Restituisce una stringa vuota se non ci sono stili collegati. |
| [get_List](../style/get_list/)() | Ottiene l'elenco che definisce la formattazione di questo stile di elenco. |
| [get_ListFormat](../style/get_listformat/)() | Fornisce l'accesso alle proprietà di formattazione dell'elenco di uno stile di paragrafo. |
| [get_Locked](../style/get_locked/)() const | Specifica se questo stile è bloccato. |
| [get_Name](../style/get_name/)() const | Ottiene o imposta il nome dello stile. |
| [get_NextParagraphStyleName](../style/get_nextparagraphstylename/)() | Ottiene/Imposta il nome dello stile da applicare automaticamente a un nuovo paragrafo inserito dopo un paragrafo formattato con lo stile specificato. |
| [get_ParagraphFormat](../style/get_paragraphformat/)() | Ottiene la formattazione del paragrafo dello stile. |
| [get_Priority](../style/get_priority/)() const | Ottiene/Imposta il valore intero che rappresenta la priorità per l'ordinamento degli stili nel riquadro attività Stili. |
| [get_RightPadding](./get_rightpadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle della tabella. |
| [get_RowStripe](./get_rowstripe/)() | Ottiene o imposta un numero di righe da includere nella striscia quando lo stile specifica la striscia di righe dispari/pari. |
| [get_SemiHidden](../style/get_semihidden/)() const | Ottiene/imposta se lo stile è nascosto dalla galleria Stili e dal riquadro attività Stili. |
| [get_Shading](./get_shading/)() | Ottiene un oggetto [Shading](../shading/) che si riferisce alla formattazione dell'ombreggiatura per le celle della tabella. |
| [get_StyleIdentifier](../style/get_styleidentifier/)() const | Ottiene l'identificatore di stile indipendente dalla locale per uno stile predefinito. |
| [get_Styles](../style/get_styles/)() const | Ottiene la raccolta di stili a cui appartiene questo stile. |
| [get_TopPadding](./get_toppadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle della tabella. |
| [get_Type](../style/get_type/)() const | Ottiene il tipo di stile (paragrafo o carattere). |
| [get_UnhideWhenUsed](../style/get_unhidewhenused/)() const | Ottiene/imposta se lo stile utilizzato nel documento corrente viene mostrato nella galleria Stili e nel riquadro attività Stili. True quando lo stile usato deve essere visualizzato nella galleria Stili. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Specifica l'allineamento verticale per le celle. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../style/remove/)() | Rimuove lo stile specificato dal documento. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Setter per [Aspose::Words::TableStyle::get_Alignment](./get_alignment/). |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Setter per [Aspose::Words::TableStyle::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_AutomaticallyUpdate](../style/set_automaticallyupdate/)(bool) | Setter per [Aspose::Words::Style::get_AutomaticallyUpdate](../style/get_automaticallyupdate/). |
| [set_BaseStyleName](../style/set_basestylename/)(const System::String\&) | Setter per [Aspose::Words::Style::get_BaseStyleName](../style/get_basestylename/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Setter per [Aspose::Words::TableStyle::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Setter per [Aspose::Words::TableStyle::get_CellSpacing](./get_cellspacing/). |
| [set_ColumnStripe](./set_columnstripe/)(int32_t) | Setter per [Aspose::Words::TableStyle::get_ColumnStripe](./get_columnstripe/). |
| [set_IsQuickStyle](../style/set_isquickstyle/)(bool) | Setter per [Aspose::Words::Style::get_IsQuickStyle](../style/get_isquickstyle/). |
| [set_LeftIndent](./set_leftindent/)(double) | Setter per [Aspose::Words::TableStyle::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Setter per [Aspose::Words::TableStyle::get_LeftPadding](./get_leftpadding/). |
| [set_LinkedStyleName](../style/set_linkedstylename/)(const System::String\&) | Impostatore per [Aspose::Words::Style::get_LinkedStyleName](../style/get_linkedstylename/). |
| [set_Locked](../style/set_locked/)(bool) | Impostatore per [Aspose::Words::Style::get_Locked](../style/get_locked/). |
| [set_Name](../style/set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Style::get_Name](../style/get_name/). |
| [set_NextParagraphStyleName](../style/set_nextparagraphstylename/)(const System::String\&) | Impostatore per [Aspose::Words::Style::get_NextParagraphStyleName](../style/get_nextparagraphstylename/). |
| [set_Priority](../style/set_priority/)(int32_t) | Impostatore per [Aspose::Words::Style::get_Priority](../style/get_priority/). |
| [set_RightPadding](./set_rightpadding/)(double) | Impostatore per [Aspose::Words::TableStyle::get_RightPadding](./get_rightpadding/). |
| [set_RowStripe](./set_rowstripe/)(int32_t) | Impostatore per [Aspose::Words::TableStyle::get_RowStripe](./get_rowstripe/). |
| [set_SemiHidden](../style/set_semihidden/)(bool) | Impostatore per [Aspose::Words::Style::get_SemiHidden](../style/get_semihidden/). |
| [set_TopPadding](./set_toppadding/)(double) | Impostatore per [Aspose::Words::TableStyle::get_TopPadding](./get_toppadding/). |
| [set_UnhideWhenUsed](../style/set_unhidewhenused/)(bool) | Impostatore per [Aspose::Words::Style::get_UnhideWhenUsed](../style/get_unhidewhenused/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Impostatore per [Aspose::Words::TableStyle::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come creare impostazioni di stile personalizzate per la tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// Impostare le proprietà di stile di una tabella può influire sulle proprietà della stessa tabella.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Vedi anche

* Class [Style](../style/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
