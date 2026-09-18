---
title: "Aspose::Words::TableStyle Klasse"
linktitle: "TableStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TableStyle Klasse. Stellt einen Tabellenstil dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 67000
url: /de/cpp/aspose.words/tablestyle/
---
## TableStyle class


Stellt einen Tabellenstil dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableStyle : public Aspose::Words::Style,
                   public Aspose::Words::ICellAttrSource,
                   public Aspose::Words::IRowAttrSource,
                   public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Equals](../style/equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Vergleicht mit dem angegebenen Stil. Stil‑IDs werden nur für integrierte Stile verglichen. Standard‑Stile sind im Vergleich nicht enthalten. Basisstil, verknüpfter Stil und nächster Absatzstil werden rekursiv verglichen. |
| [get_Aliases](../style/get_aliases/)() | Ruft alle Aliase dieses Stils ab. Wenn der Stil keine Aliase hat, wird ein leeres String‑Array zurückgegeben. |
| [get_Alignment](./get_alignment/)() | Gibt die Ausrichtung für den Tabellenstil an. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Ruft ab oder legt fest, ob Text in einer Tabellenzeile über einen Seitenumbruch hinweg aufgeteilt werden darf. |
| [get_AutomaticallyUpdate](../style/get_automaticallyupdate/)() const | Gibt an, ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird. |
| [get_BaseStyleName](../style/get_basestylename/)() | Ruft den Namen des Stils ab bzw. legt ihn fest, auf dem dieser Stil basiert. |
| [get_Borders](./get_borders/)() | Ruft die Sammlung der Standardzellenränder für den Stil ab. |
| [get_BottomPadding](./get_bottompadding/)() | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der unter dem Inhalt von Tabellenzellen hinzugefügt wird. |
| [get_BuiltIn](../style/get_builtin/)() | Wahr, wenn dieser Stil einer der integrierten Stile in MS Word ist. |
| [get_CellSpacing](./get_cellspacing/)() | Ruft ab oder legt den Abstand (in Punkten) zwischen den Zellen fest. |
| [get_ColumnStripe](./get_columnstripe/)() | Ruft ab oder legt die Anzahl der Spalten fest, die beim Banden berücksichtigt werden, wenn der Stil ungerade/gerade Spaltenbänderung angibt. |
| [get_ConditionalStyles](./get_conditionalstyles/)() | Sammlung von bedingten Stilen, die für diesen Tabellenstil definiert werden können. |
| [get_Document](../style/get_document/)() | Ermittelt das übergeordnete Dokument. |
| [get_Font](../style/get_font/)() | Ruft die Zeichenformatierung des Stils ab. |
| [get_IsHeading](../style/get_isheading/)() | Wahr, wenn der Stil einer der integrierten Überschrifts‑Stile ist. |
| [get_IsQuickStyle](../style/get_isquickstyle/)() const | Gibt an, ob dieser Stil in der Schnell-[Style](../style/)-Galerie in der MS‑Word‑Benutzeroberfläche angezeigt wird. |
| [get_LeftIndent](./get_leftindent/)() | Ruft ab oder legt den Wert fest, der den linken Einzug einer Tabelle darstellt. |
| [get_LeftPadding](./get_leftpadding/)() | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der links vom Inhalt von Tabellenzellen hinzugefügt wird. |
| [get_LinkedStyleName](../style/get_linkedstylename/)() | Ruft ab/legt den Namen des mit diesem verknüpften [Style](../style/) fest. Gibt einen leeren String zurück, wenn keine Stile verknüpft sind. |
| [get_List](../style/get_list/)() | Ruft die Liste ab, die die Formatierung dieses Listenstils definiert. |
| [get_ListFormat](../style/get_listformat/)() | Bietet Zugriff auf die Listformatierungseigenschaften eines Absatzstils. |
| [get_Locked](../style/get_locked/)() const | Gibt an, ob dieser Stil gesperrt ist. |
| [get_Name](../style/get_name/)() const | Ruft den Namen des Stils ab bzw. legt ihn fest. |
| [get_NextParagraphStyleName](../style/get_nextparagraphstylename/)() | Liest/Setzt den Namen des Stils, der automatisch auf einen neuen Absatz angewendet wird, der nach einem mit dem angegebenen Stil formatierten Absatz eingefügt wird. |
| [get_ParagraphFormat](../style/get_paragraphformat/)() | Liest die Absatzformatierung des Stils. |
| [get_Priority](../style/get_priority/)() const | Liest/Setzt den ganzzahligen Wert, der die Priorität für die Sortierung der Stile im Aufgabenbereich Stile darstellt. |
| [get_RightPadding](./get_rightpadding/)() | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der rechts vom Inhalt von Tabellenzellen hinzugefügt wird. |
| [get_RowStripe](./get_rowstripe/)() | Ruft ab oder legt die Anzahl der Zeilen fest, die beim Banden berücksichtigt werden, wenn der Stil ungerade/gerade Zeilenbänderung angibt. |
| [get_SemiHidden](../style/get_semihidden/)() const | Liest/Setzt, ob der Stil in der Stile-Galerie und im Aufgabenbereich Stile ausgeblendet wird. |
| [get_Shading](./get_shading/)() | Ruft ein [Shading](../shading/) Objekt ab, das sich auf die Schattierungsformatierung für Tabellenzellen bezieht. |
| [get_StyleIdentifier](../style/get_styleidentifier/)() const | Liest den sprachunabhängigen Stilbezeichner für einen integrierten Stil. |
| [get_Styles](../style/get_styles/)() const | Liest die Sammlung von Stilen, zu denen dieser Stil gehört. |
| [get_TopPadding](./get_toppadding/)() | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der über dem Inhalt von Tabellenzellen hinzugefügt wird. |
| [get_Type](../style/get_type/)() const | Liest den Stiltyp (Absatz oder Zeichen). |
| [get_UnhideWhenUsed](../style/get_unhidewhenused/)() const | Liest/Setzt, ob der im aktuellen Dokument verwendete Stil in der Stile-Galerie und im Aufgabenbereich Stile wieder eingeblendet wird. Wahr, wenn der verwendete Stil in der Stile-Galerie angezeigt werden soll. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Gibt die vertikale Ausrichtung für die Zellen an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../style/remove/)() | Entfernt den angegebenen Stil aus dem Dokument. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Setter für [Aspose::Words::TableStyle::get_Alignment](./get_alignment/). |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Setter für [Aspose::Words::TableStyle::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_AutomaticallyUpdate](../style/set_automaticallyupdate/)(bool) | Setter für [Aspose::Words::Style::get_AutomaticallyUpdate](../style/get_automaticallyupdate/). |
| [set_BaseStyleName](../style/set_basestylename/)(const System::String\&) | Setter für [Aspose::Words::Style::get_BaseStyleName](../style/get_basestylename/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Setter für [Aspose::Words::TableStyle::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Setter für [Aspose::Words::TableStyle::get_CellSpacing](./get_cellspacing/). |
| [set_ColumnStripe](./set_columnstripe/)(int32_t) | Setter für [Aspose::Words::TableStyle::get_ColumnStripe](./get_columnstripe/). |
| [set_IsQuickStyle](../style/set_isquickstyle/)(bool) | Setter für [Aspose::Words::Style::get_IsQuickStyle](../style/get_isquickstyle/). |
| [set_LeftIndent](./set_leftindent/)(double) | Setter für [Aspose::Words::TableStyle::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Setter für [Aspose::Words::TableStyle::get_LeftPadding](./get_leftpadding/). |
| [set_LinkedStyleName](../style/set_linkedstylename/)(const System::String\&) | Setter für [Aspose::Words::Style::get_LinkedStyleName](../style/get_linkedstylename/). |
| [set_Locked](../style/set_locked/)(bool) | Setter für [Aspose::Words::Style::get_Locked](../style/get_locked/). |
| [set_Name](../style/set_name/)(const System::String\&) | Setter für [Aspose::Words::Style::get_Name](../style/get_name/). |
| [set_NextParagraphStyleName](../style/set_nextparagraphstylename/)(const System::String\&) | Setter für [Aspose::Words::Style::get_NextParagraphStyleName](../style/get_nextparagraphstylename/). |
| [set_Priority](../style/set_priority/)(int32_t) | Setter für [Aspose::Words::Style::get_Priority](../style/get_priority/). |
| [set_RightPadding](./set_rightpadding/)(double) | Setter für [Aspose::Words::TableStyle::get_RightPadding](./get_rightpadding/). |
| [set_RowStripe](./set_rowstripe/)(int32_t) | Setter für [Aspose::Words::TableStyle::get_RowStripe](./get_rowstripe/). |
| [set_SemiHidden](../style/set_semihidden/)(bool) | Setter für [Aspose::Words::Style::get_SemiHidden](../style/get_semihidden/). |
| [set_TopPadding](./set_toppadding/)(double) | Setter für [Aspose::Words::TableStyle::get_TopPadding](./get_toppadding/). |
| [set_UnhideWhenUsed](../style/set_unhidewhenused/)(bool) | Setter für [Aspose::Words::Style::get_UnhideWhenUsed](../style/get_unhidewhenused/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Setter für [Aspose::Words::TableStyle::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie benutzerdefinierte Stileinstellungen für die Tabelle erstellt werden.
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

// Das Festlegen der Stil‑Eigenschaften einer Tabelle kann die Eigenschaften der Tabelle selbst beeinflussen.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Siehe auch

* Class [Style](../style/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
