---
title: Class DocumentBuilder
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.DocumentBuilder klas. Bietet Methoden zum Einfügen von Text Bildern und anderen Inhalten sowie zum Festlegen von Schriftarten Absatz und Abschnittsformatierungen.
type: docs
weight: 450
url: /de/net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Bietet Methoden zum Einfügen von Text, Bildern und anderen Inhalten sowie zum Festlegen von Schriftarten, Absatz- und Abschnittsformatierungen.

Um mehr zu erfahren, besuchen Sie die[Übersicht über den Document Builder](https://docs.aspose.com/words/net/document-builder-overview/) Dokumentationsartikel.

```csharp
public class DocumentBuilder
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [DocumentBuilder](documentbuilder/#constructor)() | Initialisiert eine neue Instanz dieser Klasse. |
| [DocumentBuilder](documentbuilder/#constructor_1)(Document) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bold](../../aspose.words/documentbuilder/bold/) { get; set; } | True, wenn die Schriftart fett formatiert ist. |
| [CellFormat](../../aspose.words/documentbuilder/cellformat/) { get; } | Gibt ein Objekt zurück, das die aktuellen Formatierungseigenschaften der Tabellenzelle darstellt. |
| [CurrentNode](../../aspose.words/documentbuilder/currentnode/) { get; } | Ruft den Knoten ab, der aktuell in diesem DocumentBuilder ausgewählt ist. |
| [CurrentParagraph](../../aspose.words/documentbuilder/currentparagraph/) { get; } | Ruft den Absatz ab, der aktuell darin ausgewählt ist`DocumentBuilder` . |
| [CurrentSection](../../aspose.words/documentbuilder/currentsection/) { get; } | Ruft den Abschnitt ab, der aktuell darin ausgewählt ist`DocumentBuilder` . |
| [CurrentStory](../../aspose.words/documentbuilder/currentstory/) { get; } | Ruft die aktuell ausgewählte Story ab`DocumentBuilder` . |
| [CurrentStructuredDocumentTag](../../aspose.words/documentbuilder/currentstructureddocumenttag/) { get; } | Ruft das strukturierte Dokument-Tag ab, das derzeit hier ausgewählt ist`DocumentBuilder` . |
| [Document](../../aspose.words/documentbuilder/document/) { get; set; } | Ruft das ab oder legt es fest[`Document`](./document/)Objekt, an das dieses Objekt angehängt ist. |
| [Font](../../aspose.words/documentbuilder/font/) { get; } | Gibt ein Objekt zurück, das die aktuellen Schriftartformatierungseigenschaften darstellt. |
| [IsAtEndOfParagraph](../../aspose.words/documentbuilder/isatendofparagraph/) { get; } | Gibt zurück`WAHR` wenn sich der Cursor am Ende des aktuellen Absatzes befindet. |
| [IsAtEndOfStructuredDocumentTag](../../aspose.words/documentbuilder/isatendofstructureddocumenttag/) { get; } | Gibt zurück **WAHR** wenn sich der Cursor am Ende eines strukturierten Dokument-Tags befindet. |
| [IsAtStartOfParagraph](../../aspose.words/documentbuilder/isatstartofparagraph/) { get; } | Gibt zurück`WAHR` wenn sich der Cursor am Anfang des aktuellen Absatzes befindet (kein Text vor dem Cursor). |
| [Italic](../../aspose.words/documentbuilder/italic/) { get; set; } | True, wenn die Schriftart kursiv formatiert ist. |
| [ListFormat](../../aspose.words/documentbuilder/listformat/) { get; } | Gibt ein Objekt zurück, das die aktuellen Listenformatierungseigenschaften darstellt. |
| [PageSetup](../../aspose.words/documentbuilder/pagesetup/) { get; } | Gibt ein Objekt zurück, das die aktuellen Seiteneinstellungen und Abschnittseigenschaften darstellt. |
| [ParagraphFormat](../../aspose.words/documentbuilder/paragraphformat/) { get; } | Gibt ein Objekt zurück, das die aktuellen Absatzformatierungseigenschaften darstellt. |
| [RowFormat](../../aspose.words/documentbuilder/rowformat/) { get; } | Gibt ein Objekt zurück, das die Formatierungseigenschaften der aktuellen Tabellenzeile darstellt. |
| [Underline](../../aspose.words/documentbuilder/underline/) { get; set; } | Ruft den Unterstreichungstyp für die aktuelle Schriftart ab bzw. legt diesen fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [DeleteRow](../../aspose.words/documentbuilder/deleterow/)(int, int) | Löscht eine Zeile aus einer Tabelle. |
| [EndBookmark](../../aspose.words/documentbuilder/endbookmark/)(string) | Markiert die aktuelle Position im Dokument als Lesezeichenende. |
| [EndColumnBookmark](../../aspose.words/documentbuilder/endcolumnbookmark/)(string) | Markiert die aktuelle Position im Dokument als Spalten-Lesezeichenende. Die Position muss in einer Tabellenzelle liegen. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange)() | Markiert die aktuelle Position im Dokument als bearbeitbares Bereichsende. |
| [EndEditableRange](../../aspose.words/documentbuilder/endeditablerange/#endeditablerange_1)(EditableRangeStart) | Markiert die aktuelle Position im Dokument als bearbeitbares Bereichsende. |
| [EndRow](../../aspose.words/documentbuilder/endrow/)() | Beendet eine Tabellenzeile im Dokument. |
| [EndTable](../../aspose.words/documentbuilder/endtable/)() | Beendet eine Tabelle im Dokument. |
| [InsertBreak](../../aspose.words/documentbuilder/insertbreak/)(BreakType) | Fügt einen Umbruch des angegebenen Typs in das Dokument ein. |
| [InsertCell](../../aspose.words/documentbuilder/insertcell/)() | Fügt eine Tabellenzelle in das Dokument ein. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart_1)(ChartType, double, double) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertChart](../../aspose.words/documentbuilder/insertchart/#insertchart)(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox_1)(string, bool, int) | Fügt ein Kontrollkästchen-Formularfeld an der aktuellen Position ein. |
| [InsertCheckBox](../../aspose.words/documentbuilder/insertcheckbox/#insertcheckbox)(string, bool, bool, int) | Fügt ein Kontrollkästchen-Formularfeld an der aktuellen Position ein. |
| [InsertComboBox](../../aspose.words/documentbuilder/insertcombobox/)(string, string[], int) | Fügt ein Combobox-Formularfeld an der aktuellen Position ein. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument)(Document, ImportFormatMode) | Fügt ein Dokument an der Cursorposition ein. |
| [InsertDocument](../../aspose.words/documentbuilder/insertdocument/#insertdocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Fügt ein Dokument an der Cursorposition ein. |
| [InsertDocumentInline](../../aspose.words/documentbuilder/insertdocumentinline/)(Document, ImportFormatMode, ImportFormatOptions) |  |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_1)(string) | Fügt ein Word-Feld in ein Dokument ein und aktualisiert das Feldergebnis. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield)(FieldType, bool) | Fügt ein Word-Feld in ein Dokument ein und aktualisiert optional das Feldergebnis. |
| [InsertField](../../aspose.words/documentbuilder/insertfield/#insertfield_2)(string, string) | Fügt ein Word-Feld in ein Dokument ein, ohne das Feldergebnis zu aktualisieren. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote)(FootnoteType, string) | Fügt eine Fußnote oder Endnote in das Dokument ein. |
| [InsertFootnote](../../aspose.words/documentbuilder/insertfootnote/#insertfootnote_1)(FootnoteType, string, string) | Fügt eine Fußnote oder Endnote in das Dokument ein. |
| [InsertHorizontalRule](../../aspose.words/documentbuilder/inserthorizontalrule/)() | Fügt eine horizontale Regelform in das Dokument ein. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml)(string) | Fügt einen HTML-String in das Dokument ein. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_2)(string, bool) | Fügt einen HTML-String in das Dokument ein. |
| [InsertHtml](../../aspose.words/documentbuilder/inserthtml/#inserthtml_1)(string, HtmlInsertOptions) | Fügt eine HTML-Zeichenfolge in das Dokument ein. Ermöglicht die Angabe zusätzlicher Optionen. |
| [InsertHyperlink](../../aspose.words/documentbuilder/inserthyperlink/)(string, string, bool) | Fügt einen Hyperlink in das Dokument ein. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage)(byte[]) | Fügt ein Bild aus einem Byte-Array in das Dokument ein. Das Bild wird inline und im Maßstab 100 % eingefügt. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_3)(Image) | Fügt ein Bild aus einem .NET einImage -Objekt in das Dokument einfügen. Das Bild wird inline und im Maßstab 100 % eingefügt. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_6)(Stream) | Fügt ein Bild aus einem Stream in das Dokument ein. Das Bild wird inline und im Maßstab 100 % eingefügt. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_9)(string) | Fügt ein Bild aus einer Datei oder URL in das Dokument ein. Das Bild wird inline und im Maßstab 100 % eingefügt. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_2)(byte[], double, double) | Fügt ein Inline-Bild aus einem Byte-Array in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_5)(Image, double, double) | Fügt ein Inline-Bild aus einem .NET einImage -Objekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_8)(Stream, double, double) | Fügt ein Inline-Bild aus einem Stream in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_11)(string, double, double) | Fügt ein Inline-Bild aus einer Datei oder URL in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_1)(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Fügt ein Bild aus einem Byte-Array an der angegebenen Position und Größe ein. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_4)(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Fügt ein Bild aus einem .NET einImage Objekt an der angegebenen Position und Größe. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_7)(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Fügt ein Bild aus einem Stream an der angegebenen Position und Größe ein. |
| [InsertImage](../../aspose.words/documentbuilder/insertimage/#insertimage_10)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Fügt ein Bild aus einer Datei oder URL an der angegebenen Position und Größe ein. |
| [InsertNode](../../aspose.words/documentbuilder/insertnode/)(Node) | Fügt einen Knoten vor dem Cursor ein. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject)(Stream, string, bool, Stream) | Fügt ein eingebettetes OLE-Objekt aus einem Stream in das Dokument ein. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_1)(string, bool, bool, Stream) | Fügt ein eingebettetes oder verknüpftes OLE-Objekt aus einer Datei in das Dokument ein. Erkennt den OLE-Objekttyp anhand der Dateierweiterung. |
| [InsertOleObject](../../aspose.words/documentbuilder/insertoleobject/#insertoleobject_2)(string, string, bool, bool, Stream) | Fügt ein eingebettetes oder verknüpftes OLE-Objekt aus einer Datei in das Dokument ein. Erkennt den OLE-Objekttyp mithilfe des angegebenen progID-Parameters. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon)(Stream, string, string, string) | Fügt ein eingebettetes OLE-Objekt als Symbol aus einem Stream in das Dokument ein. Ermöglicht die Angabe einer Symboldatei und einer Beschriftung. Erkennt den OLE-Objekttyp mithilfe des angegebenen progID-Parameters. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_1)(string, bool, string, string) | Fügt ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument ein. Ermöglicht die Angabe einer Symboldatei und einer Beschriftung. Erkennt den OLE-Objekttyp anhand der Dateierweiterung. |
| [InsertOleObjectAsIcon](../../aspose.words/documentbuilder/insertoleobjectasicon/#insertoleobjectasicon_2)(string, string, bool, string, string) | Fügt ein eingebettetes oder verknüpftes OLE-Objekt als Symbol in das Dokument ein. Ermöglicht die Angabe einer Symboldatei und einer Beschriftung. Erkennt den OLE-Objekttyp mithilfe des angegebenen progID-Parameters. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_1)(string, double, double) | Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_3)(string, string, byte[], double, double) | Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo)(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertOnlineVideo](../../aspose.words/documentbuilder/insertonlinevideo/#insertonlinevideo_2)(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Fügt ein Online-Videoobjekt in das Dokument ein und skaliert es auf die angegebene Größe. |
| [InsertParagraph](../../aspose.words/documentbuilder/insertparagraph/)() | Fügt einen Absatzumbruch in das Dokument ein. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape_1)(ShapeType, double, double) | Fügt eine Inline-Form mit dem angegebenen Typ und der angegebenen Größe ein. |
| [InsertShape](../../aspose.words/documentbuilder/insertshape/#insertshape)(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) | Fügt eine frei schwebende Form mit angegebener Position, Größe und Textumbruchtyp ein. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline)(SignatureLineOptions) | Fügt eine Signaturzeile an der aktuellen Position ein. |
| [InsertSignatureLine](../../aspose.words/documentbuilder/insertsignatureline/#insertsignatureline_1)(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) | Fügt eine Signaturzeile an der angegebenen Position ein. |
| [InsertStyleSeparator](../../aspose.words/documentbuilder/insertstyleseparator/)() | Fügt Stiltrennzeichen in das Dokument ein. |
| [InsertTableOfContents](../../aspose.words/documentbuilder/inserttableofcontents/)(string) | Fügt ein TOC-Feld (Inhaltsverzeichnis) in das Dokument ein. |
| [InsertTextInput](../../aspose.words/documentbuilder/inserttextinput/)(string, TextFormFieldType, string, string, int) | Fügt ein Textformularfeld an der aktuellen Position ein. |
| [MoveTo](../../aspose.words/documentbuilder/moveto/)(Node) | Bewegt den Cursor zu einem Inline-Knoten oder zum Ende eines Absatzes. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark)(string) | Bewegt den Cursor zu einem Lesezeichen. |
| [MoveToBookmark](../../aspose.words/documentbuilder/movetobookmark/#movetobookmark_1)(string, bool, bool) | Bewegt den Cursor mit größerer Präzision zu einem Lesezeichen. |
| [MoveToCell](../../aspose.words/documentbuilder/movetocell/)(int, int, int, int) | Bewegt den Cursor zu einer Tabellenzelle im aktuellen Abschnitt. |
| [MoveToDocumentEnd](../../aspose.words/documentbuilder/movetodocumentend/)() | Bewegt den Cursor an das Ende des Dokuments. |
| [MoveToDocumentStart](../../aspose.words/documentbuilder/movetodocumentstart/)() | Bewegt den Cursor an den Anfang des Dokuments. |
| [MoveToField](../../aspose.words/documentbuilder/movetofield/)(Field, bool) | Bewegt den Cursor auf ein Feld im Dokument. |
| [MoveToHeaderFooter](../../aspose.words/documentbuilder/movetoheaderfooter/)(HeaderFooterType) | Bewegt den Cursor an den Anfang einer Kopf- oder Fußzeile im aktuellen Abschnitt. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield)(string) | Bewegt den Cursor an eine Position direkt hinter dem angegebenen Zusammenführungsfeld und entfernt das Zusammenführungsfeld. |
| [MoveToMergeField](../../aspose.words/documentbuilder/movetomergefield/#movetomergefield_1)(string, bool, bool) | Verschiebt das Zusammenführungsfeld in das angegebene Zusammenführungsfeld. |
| [MoveToParagraph](../../aspose.words/documentbuilder/movetoparagraph/)(int, int) | Bewegt den Cursor zu einem Absatz im aktuellen Abschnitt. |
| [MoveToSection](../../aspose.words/documentbuilder/movetosection/)(int) | Bewegt den Cursor an den Anfang des Körpers in einem angegebenen Abschnitt. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag_1)(int, int) | Bewegt den Cursor zu einem strukturierten Dokument-Tag im aktuellen Abschnitt. |
| [MoveToStructuredDocumentTag](../../aspose.words/documentbuilder/movetostructureddocumenttag/#movetostructureddocumenttag)(StructuredDocumentTag, int) | Bewegt den Cursor zum Tag des strukturierten Dokuments. |
| [PopFont](../../aspose.words/documentbuilder/popfont/)() | Ruft die zuvor auf dem Stapel gespeicherte Zeichenformatierung ab. |
| [PushFont](../../aspose.words/documentbuilder/pushfont/)() | Speichert die aktuelle Zeichenformatierung auf dem Stapel. |
| [StartBookmark](../../aspose.words/documentbuilder/startbookmark/)(string) | Markiert die aktuelle Position im Dokument als Lesezeichen start. |
| [StartColumnBookmark](../../aspose.words/documentbuilder/startcolumnbookmark/)(string) | Markiert die aktuelle Position im Dokument als Spaltenanfang eines Lesezeichens. Die Position muss in einer Tabellenzelle liegen. |
| [StartEditableRange](../../aspose.words/documentbuilder/starteditablerange/)() | Markiert die aktuelle Position im Dokument als bearbeitbaren Bereichsstart. |
| [StartTable](../../aspose.words/documentbuilder/starttable/)() | Startet eine Tabelle im Dokument. |
| [Write](../../aspose.words/documentbuilder/write/)(string) | Fügt an der aktuellen Einfügeposition eine Zeichenfolge in das Dokument ein. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln)() | Fügt einen Absatzumbruch in das Dokument ein. |
| [Writeln](../../aspose.words/documentbuilder/writeln/#writeln_1)(string) | Fügt eine Zeichenfolge und einen Absatzumbruch in das Dokument ein. |

### Bemerkungen

`DocumentBuilder` macht den Prozess des Aufbaus eines[`Document`](../document/) einfacher. [`Document`](../document/) ist ein zusammengesetztes Objekt, das aus einem Knotenbaum besteht. Das direkte Einfügen von Content -Knoten in den Baum ist zwar möglich, erfordert jedoch ein gutes Verständnis der Baumstruktur. `DocumentBuilder` ist eine „Fassade“ für die komplexe Struktur von[`Document`](../document/) und erlaubt das schnelle und einfache Einfügen von Inhalten und Formatierungen.

Ein ... kreieren`DocumentBuilder` und assoziiere es mit a[`Document`](../document/).

Der`DocumentBuilder` verfügt über einen internen Cursor, in den der Text eingefügt wird , wenn Sie ihn aufrufen[`Write`](./write/) ,[`Writeln`](./writeln/) ,[`InsertBreak`](./insertbreak/) und andere Methoden. Sie können durch navigieren`DocumentBuilder` Bewegen Sie den Cursor mithilfe verschiedener MoveToXXX-Methoden an eine andere Position in einem Dokument.

Benutzen Sie die[`Font`](./font/)-Eigenschaft, um die Zeichenformatierung anzugeben, die für den gesamten Text gilt, der ab der aktuellen Position im Dokument eingefügt wird.

Benutzen Sie die[`ParagraphFormat`](./paragraphformat/) -Eigenschaft, um die Absatzformatierung für current und alle einzufügenden Absätze anzugeben.

Benutzen Sie die[`PageSetup`](./pagesetup/) -Eigenschaft, um Seiten- und Abschnittseigenschaften für den Abschnitt „current “ und alle Abschnitte anzugeben, die eingefügt werden.

Benutzen Sie die[`CellFormat`](./cellformat/) Und[`RowFormat`](./rowformat/) Eigenschaften zum Angeben Formatierungseigenschaften für Tabellenzellen und -zeilen. Benutzer die[`InsertCell`](./insertcell/) and [`EndRow`](./endrow/) Methoden zum Erstellen einer Tabelle.

Beachten Sie, dass[`Font`](./font/) ,[`ParagraphFormat`](./paragraphformat/) Und[`PageSetup`](./pagesetup/) Eigenschaften werden immer dann aktualisiert, wenn Sie zu einer anderen Stelle im Dokument navigieren, um die an der neuen Stelle verfügbaren Formatierungseigenschaften widerzuspiegeln.

### Beispiele

Zeigt, wie Sie mit einem Document Builder eine Tabelle erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Starten Sie die Tabelle und füllen Sie dann die erste Zeile mit zwei Zellen.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Rufen Sie die „EndRow“-Methode des Builders auf, um eine neue Zeile zu beginnen.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Zeigt, wie man mit DocumentBuilder Kopf- und Fußzeilen in einem Dokument erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie an, dass wir unterschiedliche Kopf- und Fußzeilen für die erste, gerade und ungerade Seite wünschen.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Erstellen Sie die Kopfzeilen und fügen Sie dann drei Seiten zum Dokument hinzu, um jeden Kopfzeilentyp anzuzeigen.
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

Zeigt, wie man eine Tabelle mit benutzerdefinierten Rändern erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Festlegen von Tabellenformatierungsoptionen für einen Dokumentersteller
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

// Wenn Sie die Formatierung ändern, wird sie auf die aktuelle Zelle angewendet.
// und alle neuen Zellen, die wir anschließend mit dem Builder erstellen.
// Dies hat keine Auswirkungen auf die Zellen, die wir zuvor hinzugefügt haben.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Zeilenhöhe erhöhen, um sie an den vertikalen Text anzupassen.
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


