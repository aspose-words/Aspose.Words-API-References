---
title: "Aspose::Words::DocumentBuilder class"
linktitle: "DocumentBuilder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder class. Stellt Methoden zum Einfügen von Text, Bildern und anderem Inhalt, zum Festlegen von Schriftart, Absatz- und Abschnittsformatierung bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 22000
url: /de/cpp/aspose.words/documentbuilder/
---
## DocumentBuilder class


Stellt Methoden zum Einfügen von Text, Bildern und anderem Inhalt sowie zum Festlegen von Schriftart-, Absatz- und Abschnittsformatierungen bereit. Weitere Informationen finden Sie im Dokumentationsartikel [Document Builder Overview](https://docs.aspose.com/words/cpp/document-builder-overview/).

```cpp
class DocumentBuilder : public Aspose::Words::IRunAttrSource,
                        public Aspose::Words::IParaAttrSource,
                        public Aspose::Words::IRowAttrSource,
                        public Aspose::Words::ICellAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [DeleteRow](./deleterow/)(int32_t, int32_t) | Löscht eine Zeile aus einer Tabelle. |
| [DocumentBuilder](./documentbuilder/)() | Initialisiert eine neue Instanz dieser Klasse. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Initialisiert eine neue Instanz dieser Klasse. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initialisiert eine neue Instanz dieser Klasse. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Initialisiert eine neue Instanz dieser Klasse. |
| [EndBookmark](./endbookmark/)(const System::String\&) | Markiert die aktuelle Position im Dokument als Lesezeichenende. |
| [EndColumnBookmark](./endcolumnbookmark/)(const System::String\&) | Markiert die aktuelle Position im Dokument als Spalten-Lesezeichenende. Die Position muss sich in einer Tabellenzelle befinden. |
| [EndEditableRange](./endeditablerange/)() | Markiert die aktuelle Position im Dokument als Ende eines bearbeitbaren Bereichs. |
| [EndEditableRange](./endeditablerange/)(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) | Markiert die aktuelle Position im Dokument als Ende eines bearbeitbaren Bereichs. |
| [EndRow](./endrow/)() | Beendet eine Tabellenzeile im Dokument. |
| [EndTable](./endtable/)() | Beendet eine Tabelle im Dokument. |
| [get_Bold](./get_bold/)() | Wahr, wenn die Schriftart fett formatiert ist. |
| [get_CellFormat](./get_cellformat/)() | Gibt ein Objekt zurück, das die aktuellen Formatierungseigenschaften einer Tabellenzelle darstellt. |
| [get_CurrentNode](./get_currentnode/)() | Ermittelt den Knoten, der derzeit in diesem [DocumentBuilder](./) ausgewählt ist. |
| [get_CurrentParagraph](./get_currentparagraph/)() | Ermittelt den Absatz, der derzeit in diesem [DocumentBuilder](./) ausgewählt ist. |
| [get_CurrentSection](./get_currentsection/)() | Ermittelt den Abschnitt, der derzeit in diesem [DocumentBuilder](./) ausgewählt ist. |
| [get_CurrentStory](./get_currentstory/)() | Ermittelt die Story, die derzeit in diesem [DocumentBuilder](./) ausgewählt ist. |
| [get_CurrentStructuredDocumentTag](./get_currentstructureddocumenttag/)() | Ermittelt das strukturierte Dokument-Tag, das derzeit in diesem [DocumentBuilder](./) ausgewählt ist. |
| [get_Document](./get_document/)() const | Liest oder setzt das [Document](./get_document/)‑Objekt, an das dieses Objekt angehängt ist. |
| [get_Font](./get_font/)() | Gibt ein Objekt zurück, das die aktuellen Schriftformatierungs‑Eigenschaften repräsentiert. |
| [get_IsAtEndOfParagraph](./get_isatendofparagraph/)() | Gibt **true** zurück, wenn sich der Cursor am Ende des aktuellen Absatzes befindet. |
| [get_IsAtEndOfStructuredDocumentTag](./get_isatendofstructureddocumenttag/)() | Gibt **true** zurück, wenn sich der Cursor am Ende eines strukturierten Dokument‑Tags befindet. |
| [get_IsAtStartOfParagraph](./get_isatstartofparagraph/)() | Gibt **true** zurück, wenn sich der Cursor am Anfang des aktuellen Absatzes befindet (kein Text vor dem Cursor). |
| [get_Italic](./get_italic/)() | True, wenn die Schrift als kursiv formatiert ist. |
| [get_ListFormat](./get_listformat/)() | Gibt ein Objekt zurück, das die aktuellen Listformatierungs‑Eigenschaften repräsentiert. |
| [get_PageSetup](./get_pagesetup/)() | Gibt ein Objekt zurück, das die aktuellen Seiteneinrichtungs‑ und Abschnittseigenschaften repräsentiert. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Gibt ein Objekt zurück, das die aktuellen Absatzformatierungs‑Eigenschaften repräsentiert. |
| [get_RowFormat](./get_rowformat/)() | Gibt ein Objekt zurück, das die aktuellen Tabellenzeilenformatierungs‑Eigenschaften repräsentiert. |
| [get_Underline](./get_underline/)() | Liest/setzt den Unterstreichungstyp für die aktuelle Schrift. |
| [GetType](./gettype/)() const override |  |
| [InsertBreak](./insertbreak/)(Aspose::Words::BreakType) | Fügt einen Umbruch des angegebenen Typs in das Dokument ein. |
| [InsertCell](./insertcell/)() | Fügt eine Tabellenzelle in das Dokument ein. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, int32_t) | Fügt ein Kontrollkästchen-Formularfeld an der aktuellen Position ein. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, bool, int32_t) | Fügt ein Kontrollkästchen-Formularfeld an der aktuellen Position ein. |
| [InsertComboBox](./insertcombobox/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, int32_t) | Fügt ein Kombinationsfeld-Formularfeld an der aktuellen Position ein. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Fügt ein Dokument an der Cursor‑Position ein. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Fügt ein Dokument an der Cursor‑Position ein. |
| [InsertDocumentInline](./insertdocumentinline/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Fügt ein Dokument inline an der Cursor‑Position ein. |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool) | Fügt ein Word‑Feld in ein Dokument ein und aktualisiert optional das Feldresultat. |
| [InsertField](./insertfield/)(const System::String\&) | Fügt ein Word‑Feld in ein Dokument ein und aktualisiert das Feldresultat. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&) | Fügt ein Word‑Feld in ein Dokument ein, ohne das Feldresultat zu aktualisieren. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&) | Fügt eine Fußnote oder Endnote in das Dokument ein. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) | Fügt eine Fußnote oder Endnote in das Dokument ein. |
| [InsertForms2OleControl](./insertforms2olecontrol/)(const System::SharedPtr\<Aspose::Words::Drawing::Ole::Forms2OleControl\>\&) | Fügt ein [Forms2OleControl](../)‑Objekt an der aktuellen Position ein. |
| [InsertGroupShape](./insertgroupshape/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Gruppiert die als Parameter übergebenen Formen in einen neuen GroupShape‑Knoten, der an der aktuellen Position eingefügt wird. |
| [InsertGroupShape](./insertgroupshape/)(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Gruppiert die als Parameter übergebenen Formen in einen neuen GroupShape-Knoten der angegebenen Größe, der an der angegebenen Position eingefügt wird. |
| [InsertHorizontalRule](./inserthorizontalrule/)() | Fügt eine horizontale Trennlinienform in das Dokument ein. |
| [InsertHtml](./inserthtml/)(const System::String\&) | Fügt eine HTML-Zeichenkette in das Dokument ein. |
| [InsertHtml](./inserthtml/)(const System::String\&, bool) | Fügt eine HTML-Zeichenkette in das Dokument ein. |
| [InsertHtml](./inserthtml/)(const System::String\&, Aspose::Words::HtmlInsertOptions) | Fügt eine HTML-Zeichenkette in das Dokument ein. Ermöglicht das Angeben zusätzlicher Optionen. |
| [InsertHyperlink](./inserthyperlink/)(const System::String\&, const System::String\&, bool) | Fügt einen Hyperlink in das Dokument ein. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Fügt ein Bild aus einem **Image**-Objekt in das Dokument ein. Das Bild wird inline und mit 100 % Skalierung eingefügt. |
| [InsertImage](./insertimage/)(const System::String\&) | Fügt ein Bild aus einer Datei oder URL in das Dokument ein. Das Bild wird inline und mit 100 % Skalierung eingefügt. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Fügt ein Bild aus einem Stream in das Dokument ein. Das Bild wird inline und mit 100 % Skalierung eingefügt. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&) | Fügt ein Bild aus einem Byte-Array in das Dokument ein. Das Bild wird inline und mit 100 % Skalierung eingefügt. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) | Fügt ein Inline‑Bild aus einem **Image**‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](./insertimage/)(const System::String\&, double, double) | Fügt ein Inline‑Bild aus einer Datei oder URL in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, double, double) | Fügt ein Inline‑Bild aus einem Stream in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, double, double) | Fügt ein Inline‑Bild aus einem Byte‑Array in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Fügt ein Bild aus einem **Image**‑Objekt an der angegebenen Position und Größe ein. |
| [InsertImage](./insertimage/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Fügt ein Bild aus einer Datei oder URL an der angegebenen Position und Größe ein. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Fügt ein Bild aus einem Stream an der angegebenen Position und Größe ein. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Fügt ein Bild aus einem Byte‑Array an der angegebenen Position und Größe ein. |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, double, double) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) |  |
| [InsertNode](./insertnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten vor dem Cursor ein. |
| [InsertOleObject](./insertoleobject/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Fügt ein eingebettetes OLE‑Objekt aus einem Stream in das Dokument ein. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Fügt ein eingebettetes oder verknüpftes OLE‑Objekt aus einer Datei in das Dokument ein. Erkennt den OLE‑Objekttyp anhand der Dateierweiterung. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Fügt ein eingebettetes oder verknüpftes OLE‑Objekt aus einer Datei in das Dokument ein. Erkennt den OLE‑Objekttyp anhand des angegebenen progID‑Parameters. |
| [InsertOleObject](./insertoleobject/)(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, bool, const System::String\&, const System::String\&) | Fügt ein eingebettetes oder verknüpftes OLE‑Objekt als Symbol in das Dokument ein. Ermöglicht das Angeben einer Symboldatei und Beschriftung. Erkennt den OLE‑Objekttyp anhand der Dateierweiterung. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) | Fügt ein eingebettetes oder verknüpftes OLE‑Objekt als Symbol in das Dokument ein. Ermöglicht das Angeben einer Symboldatei und Beschriftung. Erkennt den OLE‑Objekttyp anhand des angegebenen progID‑Parameters. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) | Fügt ein eingebettetes OLE‑Objekt als Symbol aus einem Stream in das Dokument ein. Ermöglicht das Angeben einer Symboldatei und Beschriftung. Erkennt den OLE‑Objekttyp anhand des angegebenen progID‑Parameters. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) |  |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, double, double) | Fügt ein Online‑Video‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Fügt ein Online‑Video‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) | Fügt ein Online‑Video‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Fügt ein Online‑Video‑Objekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertParagraph](./insertparagraph/)() | Fügt einen Absatzumbruch in das Dokument ein. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, double, double) | Fügt eine Inline‑Form mit angegebenem Typ und Größe ein. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Fügt eine frei schwebende Form mit angegebener Position, Größe und Textumbruchtyp ein. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) | Fügt eine Signaturzeile an der aktuellen Position ein. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) | Fügt eine Signaturzeile an der angegebenen Position ein. |
| [InsertStructuredDocumentTag](./insertstructureddocumenttag/)(Aspose::Words::Markup::SdtType) | Fügt ein [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) in das Dokument ein. |
| [InsertStyleSeparator](./insertstyleseparator/)() | Fügt ein Stiltrennzeichen in das Dokument ein. |
| [InsertTableOfContents](./inserttableofcontents/)(const System::String\&) | Fügt ein TOC‑Feld (Inhaltsverzeichnis) in das Dokument ein. |
| [InsertTextInput](./inserttextinput/)(const System::String\&, Aspose::Words::Fields::TextFormFieldType, const System::String\&, const System::String\&, int32_t) | Fügt ein Textformularfeld an der aktuellen Position ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MoveTo](./moveto/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bewegt den Cursor zu einem Inline‑Knoten oder zum Ende eines Absatzes. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&) | Bewegt den Cursor zu einem Lesezeichen. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&, bool, bool) | Bewegt den Cursor zu einem Lesezeichen mit höherer Präzision. |
| [MoveToCell](./movetocell/)(int32_t, int32_t, int32_t, int32_t) | Bewegt den Cursor zu einer Tabellenzelle im aktuellen Abschnitt. |
| [MoveToDocumentEnd](./movetodocumentend/)() | Bewegt den Cursor zum Ende des Dokuments. |
| [MoveToDocumentStart](./movetodocumentstart/)() | Bewegt den Cursor zum Anfang des Dokuments. |
| [MoveToField](./movetofield/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&, bool) | Bewegt den Cursor zu einem Feld im Dokument. |
| [MoveToHeaderFooter](./movetoheaderfooter/)(Aspose::Words::HeaderFooterType) | Bewegt den Cursor zum Anfang einer Kopf‑ oder Fußzeile im aktuellen Abschnitt. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&) | Bewegt den Cursor zu einer Position direkt hinter dem angegebenen Zusammenführungsfeld und entfernt das Zusammenführungsfeld. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&, bool, bool) | Verschiebt das Zusammenführungsfeld zum angegebenen Zusammenführungsfeld. |
| [MoveToParagraph](./movetoparagraph/)(int32_t, int32_t) | Bewegt den Cursor zu einem Absatz im aktuellen Abschnitt. |
| [MoveToSection](./movetosection/)(int32_t) | Bewegt den Cursor zum Anfang des Hauptbereichs in einem angegebenen Abschnitt. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(int32_t, int32_t) | Bewegt den Cursor zu einem strukturierten Dokument-Tag im aktuellen Abschnitt. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) | Bewegt den Cursor zum strukturierten Dokument-Tag. |
| [PopFont](./popfont/)() | Ruft die zuvor auf dem Stack gespeicherte Zeichenformatierung ab. |
| [PushFont](./pushfont/)() | Speichert die aktuelle Zeichenformatierung auf dem Stack. |
| [set_Bold](./set_bold/)(bool) | Setter für [Aspose::Words::DocumentBuilder::get_Bold](./get_bold/). |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Setter für [Aspose::Words::DocumentBuilder::get_Document](./get_document/). |
| [set_Italic](./set_italic/)(bool) | Setter für [Aspose::Words::DocumentBuilder::get_Italic](./get_italic/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Setter für [Aspose::Words::DocumentBuilder::get_Underline](./get_underline/). |
| [StartBookmark](./startbookmark/)(const System::String\&) | Markiert die aktuelle Position im Dokument als Lesezeichen‑Start. |
| [StartColumnBookmark](./startcolumnbookmark/)(const System::String\&) | Markiert die aktuelle Position im Dokument als Spalten‑Lesezeichen‑Start. Die Position muss sich in einer Tabellenzelle befinden. |
| [StartEditableRange](./starteditablerange/)() | Markiert die aktuelle Position im Dokument als editierbaren Bereichs‑Start. |
| [StartTable](./starttable/)() | Startet eine Tabelle im Dokument. |
| static [Type](./type/)() |  |
| [Write](./write/)(const System::String\&) | Fügt eine Zeichenkette in das Dokument an der aktuellen Einfügeposition ein. |
| [Writeln](./writeln/)(const System::String\&) | Fügt eine Zeichenkette und einen Absatzumbruch in das Dokument ein. |
| [Writeln](./writeln/)() | Fügt einen Absatzumbruch in das Dokument ein. |
## Hinweise


[DocumentBuilder](./) makes the process of building a [Document](../document/) easier. [Document](../document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows to insert content and formatting quickly and easily.

Erstelle einen [DocumentBuilder](./) und verknüpfe ihn mit einem [Document](../document/).

Der [DocumentBuilder](./) hat einen internen Cursor, an dem der Text eingefügt wird, wenn Sie [Write()](../), [Writeln()](../), [InsertBreak()](./insertbreak/) und andere Methoden aufrufen. Sie können den Cursor des [DocumentBuilder](./) zu einer anderen Position in einem Dokument navigieren, indem Sie verschiedene MoveToXXX‑Methoden verwenden.

Verwenden Sie die [Font](./get_font/)‑Eigenschaft, um die Zeichenformatierung festzulegen, die auf allen ab der aktuellen Position im Dokument eingefügten Text angewendet wird.

Verwenden Sie die [ParagraphFormat](./get_paragraphformat/)‑Eigenschaft, um die Absatzformatierung für den aktuellen und alle eingefügten Absätze festzulegen.

Verwenden Sie die [PageSetup](./get_pagesetup/)‑Eigenschaft, um Seiten- und Abschnittseigenschaften für den aktuellen Abschnitt und alle eingefügten Abschnitte festzulegen.

Verwenden Sie die [CellFormat](./get_cellformat/)‑ und [RowFormat](./get_rowformat/)‑Eigenschaften, um Formatierungseigenschaften für Tabellenzellen und -zeilen festzulegen. Verwenden Sie die [InsertCell](./insertcell/)‑ und [EndRow](./endrow/)‑Methoden, um eine Tabelle zu erstellen.

Beachten Sie, dass die Eigenschaften [Font](./get_font/), [ParagraphFormat](./get_paragraphformat/) und [PageSetup](./get_pagesetup/) aktualisiert werden, sobald Sie zu einer anderen Stelle im Dokument navigieren, um die dort verfügbaren Formatierungseigenschaften widerzuspiegeln.

## Beispiele



Zeigt, wie man eine Tabelle mit benutzerdefinierten Rahmen erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Festlegen von Tabellenformatierungsoptionen für einen DocumentBuilder
// wird sie auf jede Zeile und Zelle anwenden, die wir damit hinzufügen.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Das Ändern der Formatierung wird sie auf die aktuelle Zelle anwenden,
// und auf alle neuen Zellen, die wir anschließend mit dem Builder erstellen.
// Dies wird die bereits zuvor hinzugefügten Zellen nicht beeinflussen.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Erhöhen Sie die Zeilenhöhe, um den vertikalen Text anzupassen.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Zeigt, wie man einen DocumentBuilder verwendet, um eine Tabelle zu erstellen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Starten Sie die Tabelle und füllen Sie dann die erste Zeile mit zwei Zellen.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Rufen Sie die Methode "EndRow" des Builders auf, um eine neue Zeile zu beginnen.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
