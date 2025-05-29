---
title: DocumentBuilder Class
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.DocumentBuilder – Ihre Lösung zum mühelosen Einfügen von Text, Bildern und Formatierungselementen in Dokumente.
type: docs
weight: 660
url: /de/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Bietet Methoden zum Einfügen von Text, Bildern und anderen Inhalten sowie zum Festlegen der Schriftart sowie der Absatz- und Abschnittsformatierung.

Um mehr zu erfahren, besuchen Sie die[Document Builder-Übersicht](https://docs.aspose.com/words/net/document-builder-overview/) Dokumentationsartikel.

```csharp
public class DocumentBuilder
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Initialisiert eine neue Instanz dieser Klasse. |
| [DocumentBuilder](documentbuilder/#constructor_1)(*[Document](../document/)*) | Initialisiert eine neue Instanz dieser Klasse. |
| [DocumentBuilder](documentbuilder/#constructor_3)(*[DocumentBuilderOptions](../documentbuilderoptions/)*) | Initialisiert eine neue Instanz dieser Klasse. |
| [DocumentBuilder](documentbuilder/#constructor_2)(*[Document](../document/), [DocumentBuilderOptions](../documentbuilderoptions/)*) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | Wahr, wenn die Schriftart fett formatiert ist. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Gibt ein Objekt zurück, das die aktuellen Formatierungseigenschaften der Tabellenzelle darstellt. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Ruft den Knoten ab, der derzeit in diesem DocumentBuilder ausgewählt ist. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Ruft den Absatz ab, der aktuell in diesem`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Ruft den Abschnitt ab, der aktuell in diesem`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Ruft die aktuell ausgewählte Story ab.`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Ruft das strukturierte Dokument-Tag ab, das derzeit in diesem`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Ruft ab oder setzt die[`Document`](./document/) Objekt, an das dieses Objekt angehängt ist. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Gibt ein Objekt zurück, das die aktuellen Schriftformatierungseigenschaften darstellt. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Rückgaben`WAHR` wenn sich der Cursor am Ende des aktuellen Absatzes befindet. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Rückgaben**WAHR** wenn sich der Cursor am Ende eines strukturierten Dokument-Tags befindet. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Rückgaben`WAHR`wenn sich der Cursor am Anfang des aktuellen Absatzes befindet (kein Text vor dem Cursor). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | Wahr, wenn die Schriftart kursiv formatiert ist. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Gibt ein Objekt zurück, das die aktuellen Listenformatierungseigenschaften darstellt. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Gibt ein Objekt zurück, das die aktuellen Seiteneinstellungen und Abschnittseigenschaften darstellt. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Gibt ein Objekt zurück, das die aktuellen Absatzformatierungseigenschaften darstellt. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Gibt ein Objekt zurück, das die aktuellen Formatierungseigenschaften der Tabellenzeile darstellt. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Ruft den Unterstreichungstyp für die aktuelle Schriftart ab/legt ihn fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(*int, int*) | Löscht eine Zeile aus einer Tabelle. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(*string*) | Markiert die aktuelle Position im Dokument als Lesezeichenende. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(*string*) | Markiert die aktuelle Position im Dokument als Spaltenlesezeichenende. Die Position muss in einer Tabellenzelle liegen. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Markiert die aktuelle Position im Dokument als editierbares Bereichsende. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(*[EditableRangeStart](../editablerangestart/)*) | Markiert die aktuelle Position im Dokument als editierbares Bereichsende. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Beendet eine Tabellenzeile im Dokument. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Beendet eine Tabelle im Dokument. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(*[BreakType](../breaktype/)*) | Fügt einen Umbruch des angegebenen Typs in das Dokument ein. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Fügt eine Tabellenzelle in das Dokument ein. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_2)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double*) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_3)(*[ChartType](../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(*[ChartType](../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/), [ChartStyle](../../aspose.words.drawing.charts/chartstyle/)*) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(*string, bool, int*) | Fügt an der aktuellen Position ein Kontrollkästchen-Formularfeld ein. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(*string, bool, bool, int*) | Fügt an der aktuellen Position ein Kontrollkästchen-Formularfeld ein. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(*string, string[], int*) | Fügt an der aktuellen Position ein Combobox-Formularfeld ein. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(*[Document](../document/), [ImportFormatMode](../importformatmode/)*) | Fügt ein Dokument an der Cursorposition ein. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Fügt ein Dokument an der Cursorposition ein. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(*[Document](../document/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Fügt ein Dokument inline an der Cursorposition ein. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(*string*) | Fügt ein Word-Feld in ein Dokument ein und aktualisiert das Feldergebnis. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Fügt ein Word-Feld in ein Dokument ein und aktualisiert optional das Feldergebnis. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(*string, string*) | Fügt ein Word-Feld in ein Dokument ein, ohne das Feldergebnis zu aktualisieren. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string*) | Fügt eine Fußnote oder Endnote in das Dokument ein. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(*[FootnoteType](../../aspose.words.notes/footnotetype/), string, string*) | Fügt eine Fußnote oder Endnote in das Dokument ein. |
| [InsertForms2OleControl](../../aspose.words/documentbuilder/insertforms2olecontrol/)(*[Forms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/)*) | Einsätze[`Forms2OleControl`](../../aspose.words.drawing.ole/forms2olecontrol/) Objekt in aktuelle Position. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape)(*params ShapeBase[]*) | Gruppiert die als Parameter übergebenen Formen in einem neuen GroupShape-Knoten, der an der aktuellen Position eingefügt wird. |
| [InsertGroupShape](../../aspose.words/documentbuilder/insertgroupshape/#insertgroupshape_1)(*double, double, double, double, params ShapeBase[]*) | Gruppiert die als Parameter übergebenen Formen in einem neuen GroupShape-Knoten der angegebenen Größe, der an der angegebenen Position eingefügt wird. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Fügt eine horizontale Linienform in das Dokument ein. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(*string*) | Fügt eine HTML-Zeichenfolge in das Dokument ein. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(*string, bool*) | Fügt eine HTML-Zeichenfolge in das Dokument ein. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(*string, [HtmlInsertOptions](../htmlinsertoptions/)*) | Fügt einen HTML-String in das Dokument ein. Ermöglicht die Angabe zusätzlicher Optionen. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(*string, string, bool*) | Fügt einen Hyperlink in das Dokument ein. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(*byte[]*) | Fügt ein Bild aus einem Byte-Array in das Dokument ein. Das Bild wird inline und im Maßstab 100 % eingefügt. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(*Image*) | Fügt ein Bild aus einer .NETImage Objekt in das Dokument. Das Bild wird inline und im Maßstab 100 % eingefügt. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(*Stream*) | Fügt ein Bild aus einem Stream in das Dokument ein. Das Bild wird inline und im Maßstab 100 % eingefügt. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(*string*) | Fügt ein Bild aus einer Datei oder URL in das Dokument ein. Das Bild wird inline und im Maßstab 100 % eingefügt. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(*byte[], double, double*) | Fügt ein Inline-Bild aus einem Byte-Array in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(*Image, double, double*) | Fügt ein Inline-Bild aus einem .NETImage -Objekt in das Dokument und skaliert es auf die angegebene Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(*Stream, double, double*) | Fügt ein Inline-Bild aus einem Stream in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(*string, double, double*) | Fügt ein Inline-Bild aus einer Datei oder URL in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(*byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Fügt ein Bild aus einem Byte-Array an der angegebenen Position und Größe ein. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(*Image, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Fügt ein Bild aus einer .NETImage Objekt an der angegebenen Position und Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(*Stream, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Fügt ein Bild aus einem Stream an der angegebenen Position und in der angegebenen Größe ein. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Fügt ein Bild aus einer Datei oder URL an der angegebenen Position und in der angegebenen Größe ein. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(*[Node](../node/)*) | Fügt einen Knoten vor dem Cursor ein. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(*Stream, string, bool, Stream*) | Fügt ein eingebettetes OLE-Objekt aus einem Stream in das Dokument ein. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(*string, bool, bool, Stream*) | Fügt ein eingebettetes oder verknüpftes OLE-Objekt aus einer Datei in das Dokument ein. Der OLE-Objekttyp wird anhand der Dateierweiterung erkannt. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(*string, string, bool, bool, Stream*) | Fügt ein eingebettetes oder verknüpftes OLE-Objekt aus einer Datei in das Dokument ein. Der OLE-Objekttyp wird anhand des angegebenen progID-Parameters ermittelt. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(*Stream, string, string, string*) | Fügt ein eingebettetes OLE-Objekt als Symbol aus einem Stream in das Dokument ein. Ermöglicht die Angabe der Symboldatei und der Beschriftung. Erkennt den OLE-Objekttyp anhand des angegebenen progID-Parameters. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(*string, bool, string, string*) | Fügt ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument ein. Ermöglicht die Angabe der Symboldatei und der Beschriftung. Erkennt den OLE-Objekttyp anhand der Dateierweiterung. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(*string, string, bool, string, string*) | Fügt ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument ein. Ermöglicht die Angabe der Symboldatei und der Beschriftung. Erkennt den OLE-Objekttyp anhand des angegebenen progID-Parameters. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(*string, double, double*) | Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(*string, string, byte[], double, double*) | Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(*string, [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(*string, string, byte[], [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Fügt einen Absatzumbruch in das Dokument ein. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(*[ShapeType](../../aspose.words.drawing/shapetype/), double, double*) | Fügt eine Inline-Form mit angegebenem Typ und angegebener Größe ein. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(*[ShapeType](../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Fügt eine frei schwebende Form mit angegebener Position, Größe und Textumbruchart ein. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(*[SignatureLineOptions](../signaturelineoptions/)*) | Fügt an der aktuellen Position eine Signaturzeile ein. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(*[SignatureLineOptions](../signaturelineoptions/), [RelativeHorizontalPosition](../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../aspose.words.drawing/wraptype/)*) | Fügt an der angegebenen Position eine Signaturzeile ein. |
| [InsertStructuredDocumentTag](../../aspose.words/documentbuilder/insertstructureddocumenttag/)(*[SdtType](../../aspose.words.markup/sdttype/)*) | Fügt ein[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) in das Dokument. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Fügt einen Stiltrenner in das Dokument ein. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(*string*) | Fügt ein TOC-Feld (Inhaltsverzeichnis) in das Dokument ein. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(*string, [TextFormFieldType](../../aspose.words.fields/textformfieldtype/), string, string, int*) | Fügt an der aktuellen Position ein Textformularfeld ein. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(*[Node](../node/)*) | Bewegt den Cursor zu einem Inline-Knoten oder an das Ende eines Absatzes. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(*string*) | Bewegt den Cursor zu einem Lesezeichen. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(*string, bool, bool*) | Verschiebt den Cursor mit größerer Präzision zu einem Lesezeichen. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(*int, int, int, int*) | Bewegt den Cursor zu einer Tabellenzelle im aktuellen Abschnitt. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Bewegt den Cursor an das Ende des Dokuments. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Bewegt den Cursor an den Anfang des Dokuments. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(*[Field](../../aspose.words.fields/field/), bool*) | Bewegt den Cursor zu einem Feld im Dokument. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(*[HeaderFooterType](../headerfootertype/)*) | Bewegt den Cursor an den Anfang einer Kopf- oder Fußzeile im aktuellen Abschnitt. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(*string*) | Verschiebt den Cursor an eine Position direkt hinter dem angegebenen Seriendruckfeld und entfernt das Seriendruckfeld. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(*string, bool, bool*) | Verschiebt das Seriendruckfeld in das angegebene Seriendruckfeld. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(*int, int*) | Bewegt den Cursor zu einem Absatz im aktuellen Abschnitt. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(*int*) | Verschiebt den Cursor an den Anfang des Textkörpers in einem angegebenen Abschnitt. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(*int, int*) | Bewegt den Cursor zu einem strukturierten Dokument-Tag im aktuellen Abschnitt. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/), int*) | Bewegt den Cursor zum strukturierten Dokument-Tag. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Ruft die zuvor auf dem Stapel gespeicherte Zeichenformatierung ab. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Speichert die aktuelle Zeichenformatierung auf dem Stapel. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(*string*) | Markiert die aktuelle Position im Dokument als Lesezeichenanfang. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(*string*) | Markiert die aktuelle Position im Dokument als Spaltenanfang. Die Position muss in einer Tabellenzelle liegen. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Markiert die aktuelle Position im Dokument als editierbaren Bereichsanfang. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Beginnt eine Tabelle im Dokument. |
| [Write](../../aspose.words/documentbuilder/write/)(*string*) | Fügt an der aktuellen Einfügeposition eine Zeichenfolge in das Dokument ein. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Fügt einen Absatzumbruch in das Dokument ein. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(*string*) | Fügt eine Zeichenfolge und einen Absatzumbruch in das Dokument ein. |

## Bemerkungen

`DocumentBuilder` macht den Prozess des Aufbaus einer[`Document`](../document/) einfacher. [`Document`](../document/) ist ein zusammengesetztes Objekt, das aus einem Knotenbaum besteht. Obwohl das Einfügen von content Knoten direkt in den Baum möglich ist, erfordert dies ein gutes Verständnis der Baumstruktur. `DocumentBuilder` ist eine "Fassade" für die komplexe Struktur von[`Document`](../document/) und ermöglicht , Inhalte und Formatierungen schnell und einfach einzufügen.

Erstellen Sie ein`DocumentBuilder` und verknüpfen Sie es mit einem[`Document`](../document/).

Der`DocumentBuilder` hat einen internen Cursor, in den der Text eingefügt wird , wenn Sie aufrufen[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) und andere Methoden. Sie können navigieren die`DocumentBuilder` Cursor mithilfe verschiedener MoveToXXX-Methoden an eine andere Position in einem Dokument verschieben.

Verwenden Sie die[`Font`](./font/) -Eigenschaft zum Festlegen der Zeichenformatierung, die auf allen Text angewendet wird, der ab der aktuellen Position im Dokument eingefügt wird.

Verwenden Sie die[`ParagraphFormat`](./paragraphformat/) -Eigenschaft, um die Absatzformatierung für current und alle Absätze anzugeben, die eingefügt werden.

Verwenden Sie die[`PageSetup`](./pagesetup/) -Eigenschaft zum Angeben der Seiten- und Abschnittseigenschaften für den Abschnitt current und alle Abschnitte, die eingefügt werden.

Verwenden Sie die[`CellFormat`](./cellformat/) Und[`RowFormat`](./rowformat/) Eigenschaften, um die Formatierungseigenschaften für Tabellenzellen und -zeilen anzugeben. Verwenden Sie die[`InsertCell`](./insertcell/) und [`EndRow`](./endrow/) Methoden zum Erstellen einer Tabelle.

Beachten Sie, dass[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) Und[`PageSetup`](./pagesetup/) Eigenschaften werden aktualisiert, wenn Sie zu einer anderen Stelle im Dokument navigieren, um die an der neuen Position verfügbaren Formatierungseigenschaften widerzuspiegeln.

## Beispiele

Zeigt, wie Sie mit einem Dokumentgenerator eine Tabelle erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Starten Sie die Tabelle und füllen Sie dann die erste Zeile mit zwei Zellen.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Rufen Sie die Methode „EndRow“ des Builders auf, um eine neue Zeile zu beginnen.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Zeigt, wie Sie mit DocumentBuilder Kopf- und Fußzeilen in einem Dokument erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie an, dass wir für die erste, die gerade und die ungerade Seite unterschiedliche Kopf- und Fußzeilen wünschen.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Erstellen Sie die Kopfzeilen und fügen Sie dem Dokument dann drei Seiten hinzu, um jeden Kopfzeilentyp anzuzeigen.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Zeigt, wie eine Tabelle mit benutzerdefinierten Rändern erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Festlegen von Tabellenformatierungsoptionen für einen Dokumentgenerator
// wendet sie auf jede Zeile und Zelle an, die wir damit hinzufügen.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Das Ändern der Formatierung wird auf die aktuelle Zelle angewendet,
// und alle neuen Zellen, die wir anschließend mit dem Builder erstellen.
// Dies hat keine Auswirkungen auf die Zellen, die wir zuvor hinzugefügt haben.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Erhöhen Sie die Zeilenhöhe, damit der vertikale Text hineinpasst.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
