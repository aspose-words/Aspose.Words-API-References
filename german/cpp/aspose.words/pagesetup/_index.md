---
title: "Aspose::Words::PageSetup Klasse"
linktitle: "PageSetup"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup Klasse. Stellt die Seiteneinrichtungseigenschaften eines Abschnitts dar. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 46000
url: /de/cpp/aspose.words/pagesetup/
---
## PageSetup class


Stellt die Seiteneinrichtungseigenschaften eines Abschnitts dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Setzt die Seiteneinrichtung auf die Standardpapiergröße, Ränder und Ausrichtung zurück. |
| [get_Bidi](./get_bidi/)() | Gibt an, dass dieser Abschnitt bidirektionalen (komplexen Skripte) Text enthält. |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | Gibt an, wo der Seitenrand relativ zu überlappenden Texten und Objekten positioniert ist. |
| [get_BorderAppliesTo](./get_borderappliesto/)() | Gibt an, auf welchen Seiten der Seitenrand gedruckt wird. |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | Liest oder legt einen Wert fest, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umschlossenen Text gemessen wird. |
| [get_Borders](./get_borders/)() | Liefert eine Sammlung der Seitenränder. |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | Gibt an, ob der Seitenrand die Fußzeile ein- oder ausschließt. |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | Gibt an, ob der Seitenrand die Kopfzeile ein- oder ausschließt. |
| [get_BottomMargin](./get_bottommargin/)() | Gibt die Entfernung (in Punkten) zwischen dem unteren Rand der Seite und der unteren Begrenzung des Fließtextes zurück oder legt sie fest. |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | Liest oder legt das Trennzeichen fest, das zwischen der Kapitelnummer und der Seitenzahl erscheint. |
| [get_CharactersPerLine](./get_charactersperline/)() | Liest oder legt die Anzahl der Zeichen pro Zeile im Dokumentengitter fest. |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | Wahr, wenn auf der ersten Seite eine andere Kopf- oder Fußzeile verwendet wird. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Stellt Optionen bereit, die die Nummerierung und Positionierung von Endnoten in diesem Abschnitt steuern. |
| [get_FirstPageTray](./get_firstpagetray/)() | Liest das Papierfach (Behälter) aus, das für die erste Seite eines Abschnitts verwendet wird. Der Wert ist implementierungsabhängig (Drucker). |
| [get_FooterDistance](./get_footerdistance/)() | Gibt die Entfernung (in Punkten) zwischen der Fußzeile und dem unteren Rand der Seite zurück oder legt sie fest. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Stellt Optionen bereit, die die Nummerierung und Positionierung von Fußnoten in diesem Abschnitt steuern. |
| [get_Gutter](./get_gutter/)() | Liest oder legt die Menge des zusätzlichen Raums fest, der dem Rand für die Dokumentbindung hinzugefügt wird. |
| [get_HeaderDistance](./get_headerdistance/)() | Gibt die Entfernung (in Punkten) zwischen der Kopfzeile und dem oberen Rand der Seite zurück oder legt sie fest. |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | Liest oder legt den Überschriftenebenenstil fest, der auf die Kapiteltitel im Dokument angewendet wird. |
| [get_LayoutMode](./get_layoutmode/)() | Liest oder legt den Layoutmodus dieses Abschnitts fest. |
| [get_LeftMargin](./get_leftmargin/)() | Gibt die Entfernung (in Punkten) zwischen dem linken Rand der Seite und der linken Begrenzung des Fließtextes zurück oder legt sie fest. |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | Gibt die numerische Erhöhung für Zeilennummern zurück oder legt sie fest. |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | Liest oder legt den Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments fest. |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | Liest oder legt fest, wie die Zeilennummerierung verläuft, d. h. ob sie am Anfang einer neuen Seite oder eines neuen Abschnitts neu beginnt oder kontinuierlich weiterläuft. |
| [get_LinesPerPage](./get_linesperpage/)() | Liest oder legt die Anzahl der Zeilen pro Seite im Dokumentengitter fest. |
| [get_LineStartingNumber](./get_linestartingnumber/)() | Liest oder legt die Startzeilennummer fest. |
| [get_Margins](./get_margins/)() | Gibt die voreingestellten [Margins](../margins/) der Seite zurück oder legt sie fest. |
| [get_MultiplePages](./get_multiplepages/)() const | Für mehrseitige Dokumente liest oder legt fest, wie ein Dokument gedruckt oder gerendert wird, damit es als Heft gebunden werden kann. |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | Wahr, wenn das Dokument unterschiedliche Kopf- und Fußzeilen für ungerade und gerade Seiten hat. |
| [get_Orientation](./get_orientation/)() | Gibt die Ausrichtung der Seite zurück oder legt sie fest. |
| [get_OtherPagesTray](./get_otherpagestray/)() | Liest das Papierfach (Behälter) aus, das für alle Seiten außer der ersten Seite eines Abschnitts verwendet wird. Der Wert ist implementierungsabhängig (Drucker). |
| [get_PageHeight](./get_pageheight/)() | Gibt die Höhe der Seite in Punkten zurück oder legt sie fest. |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | Liest oder legt das Format der Seitenzahlen fest. |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | Liest oder legt die Startseitenzahl des Abschnitts fest. |
| [get_PageWidth](./get_pagewidth/)() | Gibt die Breite der Seite in Punkten zurück oder legt sie fest. |
| [get_PaperSize](./get_papersize/)() | Gibt die Papiergröße zurück oder legt sie fest. |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | True, wenn die Seitennummerierung am Anfang des Abschnitts neu beginnt. |
| [get_RightMargin](./get_rightmargin/)() | Gibt den Abstand (in Punkten) zwischen dem rechten Rand der Seite und der rechten Begrenzung des Fließtextes zurück oder legt ihn fest. |
| [get_RtlGutter](./get_rtlgutter/)() | Liest oder legt fest, ob Microsoft Word für den Abschnitt Ränder basierend auf einer Rechts-nach-Links- oder Links-nach-Rechts-Sprache verwendet. |
| [get_SectionStart](./get_sectionstart/)() | Gibt den Typ des Abschnittsumbruchs für das angegebene Objekt zurück oder legt ihn fest. |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | Gibt die Anzahl der Seiten zurück, die in jedem Heft enthalten sein sollen, oder legt sie fest. |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | True, wenn Endnoten am Ende des nächsten Abschnitts gedruckt werden, der Endnoten nicht unterdrückt. Unterdrückte Endnoten werden vor den Endnoten in diesem Abschnitt gedruckt. |
| [get_TextColumns](./get_textcolumns/)() | Gibt eine Sammlung zurück, die die Menge der Textspalten darstellt. |
| [get_TextOrientation](./get_textorientation/)() | Ermöglicht die Angabe von [TextOrientation](./get_textorientation/) für die gesamte Seite. Der Standardwert ist [Horizontal](../textorientation/) |
| [get_TopMargin](./get_topmargin/)() | Gibt den Abstand (in Punkten) zwischen dem oberen Rand der Seite und der oberen Begrenzung des Fließtextes zurück oder legt ihn fest. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Gibt die vertikale Ausrichtung des Textes auf jeder Seite in einem Dokument oder Abschnitt zurück oder legt sie fest. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bidi](./set_bidi/)(bool) | Setter für [Aspose::Words::PageSetup::get_Bidi](./get_bidi/). |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | Setter für [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/). |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | Setter für [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/). |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | Setter für [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/). |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | Setter für [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/). |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | Setter für [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/). |
| [set_BottomMargin](./set_bottommargin/)(double) | Setter für [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/). |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | Setter für [Aspose::Words::PageSetup::get_ChapterPageSeparator](./get_chapterpageseparator/). |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | Setter für [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/). |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | Setter für [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/). |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | Legt das Papierfach (Bin) fest, das für die erste Seite eines Abschnitts verwendet wird. Der Wert ist implementationsspezifisch (Drucker). |
| [set_FooterDistance](./set_footerdistance/)(double) | Setter für [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/). |
| [set_Gutter](./set_gutter/)(double) | Setter für [Aspose::Words::PageSetup::get_Gutter](./get_gutter/). |
| [set_HeaderDistance](./set_headerdistance/)(double) | Setter für [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | Setter für [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | Setter für [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | Setter für [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | Setter für [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | Setter für [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | Setter für [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | Setter für [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | Setter für [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_Margins](./set_margins/)(Aspose::Words::Margins) | Setter für [Aspose::Words::PageSetup::get_Margins](./get_margins/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | Setter für [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | Setter für [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | Setter für [Aspose::Words::PageSetup::get_Orientation](./get_orientation/). |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | Legt das Papierfach (Bin) fest, das für alle Seiten außer der ersten Seite eines Abschnitts verwendet wird. Der Wert ist implementationsspezifisch (Drucker). |
| [set_PageHeight](./set_pageheight/)(double) | Setter für [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/). |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | Setter für [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/). |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | Setter für [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/). |
| [set_PageWidth](./set_pagewidth/)(double) | Setter für [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/). |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | Setter für [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/). |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | Setter für [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/). |
| [set_RightMargin](./set_rightmargin/)(double) | Setter für [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/). |
| [set_RtlGutter](./set_rtlgutter/)(bool) | Setter für [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/). |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | Setter für [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/). |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | Setter für [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/). |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | True, wenn Endnoten am Ende des nächsten Abschnitts gedruckt werden, der Endnoten nicht unterdrückt. Unterdrückte Endnoten werden vor den Endnoten in diesem Abschnitt gedruckt. |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | Setter für [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/). |
| [set_TopMargin](./set_topmargin/)(double) | Setter für [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | Setter für [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |
## Hinweise


[PageSetup](./) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## Beispiele



Zeigt, wie Seiteneinrichtungseinstellungen auf Abschnitte in einem Dokument angewendet und zurückgesetzt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ändern Sie die Seiteneinrichtungseigenschaften für den aktuellen Abschnitt des Builders und fügen Sie Text hinzu.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Wenn wir einen neuen Abschnitt mit einem Dokument-Builder starten,
// erbt die aktuellen Seiteneinrichtungseigenschaften des Builders.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Wir können seine Seiteneinrichtungseigenschaften mit der Methode "ClearFormatting" auf die Standardwerte zurücksetzen.
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
