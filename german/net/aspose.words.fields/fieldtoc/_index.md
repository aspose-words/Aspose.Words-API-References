---
title: FieldToc
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das TOC-Feld.
type: docs
weight: 2380
url: /de/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Implementiert das TOC-Feld.

```csharp
public class FieldToc : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldToc](fieldtoc)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname) { get; set; } | Ruft den Namen des Lesezeichens ab oder legt ihn fest, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wurde. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel) { get; set; } | Ruft den Namen der Sequenzkennung ab oder legt ihn fest, die beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das die Beschriftung und Nummer von nicht enthält. |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles) { get; set; } | Ruft eine Liste mit anderen Stilen als den integrierten Überschriftenstilen ab oder legt sie fest, die in das Inhaltsverzeichnis aufgenommen werden sollen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier) { get; set; } | Ruft eine Zeichenfolge ab oder legt sie fest, die mit den Typkennungen der eingeschlossenen TC-Felder übereinstimmen sollte. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange) { get; set; } | Ruft einen Bereich von Ebenen der einzuschließenden Inhaltsverzeichniseinträge ab oder legt diesen fest. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator) { get; set; } | Ruft eine Folge von Zeichen ab oder legt sie fest, die einen Eintrag und seine Seitenzahl trennt. |
| [Format](../../aspose.words.fields/field/format) { get; } | erhält a[`FieldFormat`](../fieldformat) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange) { get; set; } | Ruft einen Bereich von einzubeziehenden Überschriftenebenen ab oder legt diesen fest. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout) { get; set; } | Ruft ab oder legt fest, ob Tabulator-Leerzeichen und Seitenzahlen in der Weblayoutansicht ausgeblendet werden sollen. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks) { get; set; } | Ruft ab oder legt fest, ob Hyperlinks zu den Inhaltsverzeichniseinträgen erstellt werden sollen. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange) { get; set; } | Ruft einen Bereich von Ebenen der Einträge im Inhaltsverzeichnis ab oder legt diesen fest, bei denen Seitenzahlen weggelassen werden sollen. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier) { get; set; } | Ruft die Kennung einer Sequenz ab oder setzt sie, für die ein Präfix zur Seitenzahl des Eintrags hinzugefügt werden soll. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks) { get; set; } | Ruft ab oder legt fest, ob Zeilenumbrüche in Tabelleneinträgen beibehalten werden sollen. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs) { get; set; } | Ruft ab oder legt fest, ob Tabulatoreinträge in Tabelleneinträgen beibehalten werden sollen. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel) { get; set; } | Ruft den Namen der Sequenzkennung ab, die beim Erstellen eines Abbildungsverzeichnisses verwendet wird, oder legt ihn fest. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel) { get; set; } | Ruft ab oder legt fest, ob die angewendete Absatzgliederungsebene verwendet werden soll. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers)() | Aktualisiert die Seitenzahlen für Elemente in diesem Inhaltsverzeichnis. |

### Bemerkungen

Erstellt ein Inhaltsverzeichnis (das auch ein Abbildungsverzeichnis sein kann) unter Verwendung der durch TC-Felder angegebenen Einträge, ihrer Überschriftenebenen und angegebenen Stile und fügt diese Tabelle an dieser Stelle in das Dokument ein.

### Beispiele

Zeigt, wie ein Inhaltsverzeichnis eingefügt und mit Einträgen auf der Grundlage von Überschriftenstilen gefüllt wird.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Füge ein TOC-Feld ein, das alle Überschriften zu einem Inhaltsverzeichnis zusammenstellt.
    // Für jede Überschrift erstellt dieses Feld eine Zeile mit dem Text in diesem Überschriftenstil auf der linken Seite,
    // und die Seite, auf der die Überschrift erscheint, rechts.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Verwenden Sie die BookmarkName-Eigenschaft, um nur Überschriften aufzulisten
    // die innerhalb der Grenzen eines Lesezeichens mit dem Namen "MyBookmark" erscheinen.
    field.BookmarkName = "MyBookmark";

    // Text mit einem integrierten Überschriftenstil, wie z. B. "Überschrift 1", der darauf angewendet wird, zählt als Überschrift.
    // Wir können zusätzliche Stile benennen, die als Überschriften vom Inhaltsverzeichnis in dieser Eigenschaft und ihren Inhaltsverzeichnisebenen aufgenommen werden sollen.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Standardmäßig werden Styles/TOC-Ebenen in der CustomStyles-Eigenschaft durch ein Komma getrennt,
    // aber wir können in dieser Eigenschaft ein benutzerdefiniertes Trennzeichen setzen.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Konfigurieren Sie das Feld so, dass alle Überschriften ausgeschlossen werden, deren Inhaltsverzeichnis außerhalb dieses Bereichs liegt.
    field.HeadingLevelRange = "1-3";

    // Das Inhaltsverzeichnis zeigt nicht die Seitenzahlen von Überschriften an, deren Inhaltsverzeichnisebenen innerhalb dieses Bereichs liegen.
    field.PageNumberOmittingLevelRange = "2-5";

     // Legen Sie eine benutzerdefinierte Zeichenfolge fest, die jede Überschrift von ihrer Seitenzahl trennt.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Bei diesen beiden Überschriften werden die Seitenzahlen weggelassen, da sie im Bereich "2-5" liegen.
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Dieser Eintrag erscheint nicht, da "Überschrift 4" außerhalb des Bereichs "1-3" liegt, den wir zuvor festgelegt haben.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Dieser Eintrag wird nicht angezeigt, da er sich außerhalb des vom Inhaltsverzeichnis angegebenen Lesezeichens befindet.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");

/// <summary>
/// Beginne eine neue Seite und füge einen Absatz eines bestimmten Stils ein.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

Zeigt, wie ein TOC-Feld mithilfe von SEQ-Feldern mit Einträgen gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein TOC-Feld kann einen Eintrag in seinem Inhaltsverzeichnis für jedes im Dokument gefundene SEQ-Feld erstellen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält, und die Seitennummer, auf der das Feld erscheint.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ-Felder zeigen einen Zähler an, der sich bei jedem SEQ-Feld erhöht.
// Diese Felder verwalten auch separate Zählwerte für jede eindeutig benannte Sequenz
// identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Felds.
// Verwenden Sie die Eigenschaft "TableOfFiguresLabel", um eine Hauptsequenz für das Inhaltsverzeichnis zu benennen.
// Jetzt erstellt dieses Inhaltsverzeichnis nur Einträge aus SEQ-Feldern, deren "SequenceIdentifier" auf "MySequence" gesetzt ist.
fieldToc.TableOfFiguresLabel = "MySequence";

// Wir können in der Eigenschaft "PrefixedSequenceIdentifier" eine andere SEQ-Feldsequenz benennen.
 // SEQ-Felder aus dieser Präfixsequenz erstellen keine TOC-Einträge.
// Jeder TOC-Eintrag, der aus einem SEQ-Feld der Hauptsequenz erstellt wurde, zeigt jetzt auch die Anzahl dieser an
// Die Präfixsequenz ist derzeit im SEQ-Feld der Primärsequenz aktiviert, das den Eintrag vorgenommen hat.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Jeder TOC-Eintrag zeigt die Anzahl der Präfixsequenzen unmittelbar links davon an
// der Seitennummer, auf der das SEQ-Feld der Hauptsequenz erscheint.
// Wir können ein benutzerdefiniertes Trennzeichen angeben, das zwischen diesen beiden Zahlen erscheint.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Es gibt zwei Möglichkeiten, SEQ-Felder zu verwenden, um dieses Inhaltsverzeichnis zu füllen.
// 1 - Einfügen eines SEQ-Felds, das zur Präfixsequenz des Inhaltsverzeichnisses gehört:
// Dieses Feld erhöht den SEQ-Sequenzzähler für die "PrefixSequence" um 1.
// Da dieses Feld nicht zur identifizierten Hauptfolge gehört
// durch die Eigenschaft "TableOfFiguresLabel" des Inhaltsverzeichnisses wird es nicht als Eintrag angezeigt.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Einfügen eines SEQ-Felds, das zur Hauptsequenz des Inhaltsverzeichnisses gehört:
// Dieses SEQ-Feld erstellt einen Eintrag im Inhaltsverzeichnis.
// Der TOC-Eintrag enthält den Absatz, in dem sich das SEQ-Feld befindet, und die Nummer der Seite, auf der es erscheint.
// Dieser Eintrag zeigt auch den Zähler an, bei dem sich die Präfixsequenz derzeit befindet,
// getrennt von der Seitenzahl durch den Wert in der Eigenschaft SequenceSeparator des Inhaltsverzeichnisses.
// Der "PrefixSequence"-Zähler ist auf 1, dieses SEQ-Feld der Hauptsequenz befindet sich auf Seite 2,
// und das Trennzeichen ist ">", sodass der Eintrag "1>2" anzeigt.
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Eine Seite einfügen, die Präfixsequenz um 2 vorrücken und ein SEQ-Feld einfügen, um danach einen TOC-Eintrag zu erstellen.
// Die Präfixsequenz ist jetzt bei 2 und das SEQ-Feld der Hauptsequenz befindet sich auf Seite 3,
// Der TOC-Eintrag zeigt also "2>3" bei seiner Seitenzahl an.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Siehe auch

* class [Field](../field)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
