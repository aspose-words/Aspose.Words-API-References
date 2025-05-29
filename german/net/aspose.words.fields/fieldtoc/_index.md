---
title: FieldToc Class
linktitle: FieldToc
articleTitle: FieldToc
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldToc für die nahtlose Erstellung von Inhaltsverzeichnissen in Dokumenten. Verbessern Sie Ihren Workflow mit leistungsstarken Funktionen!
type: docs
weight: 2940
url: /de/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Implementiert das TOC-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldToc : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldToc](fieldtoc/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname/) { get; set; } | Ruft den Namen des Lesezeichens ab oder legt ihn fest, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wurde. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | Ruft den Namen der Sequenzkennung ab oder legt ihn fest, die beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das weder Beschriftung noch Nummer der Bildunterschrift enthält. |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | Ruft eine Liste mit anderen Stilen als den integrierten Überschriftenstilen ab oder legt diese fest, die in das Inhaltsverzeichnis aufgenommen werden sollen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | Ruft eine Zeichenfolge ab oder legt sie fest, die mit den Typkennungen der einzuschließenden TC-Felder übereinstimmen soll. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | Ruft einen Ebenenbereich der einzuschließenden Inhaltsverzeichniseinträge ab oder legt diesen fest. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | Ruft eine Zeichenfolge ab oder legt sie fest, die einen Eintrag und seine Seitenzahl trennt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | Ruft einen Bereich einzuschließender Überschriftenebenen ab oder legt diesen fest. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | Ruft ab oder legt fest, ob Tabulatorenführer und Seitenzahlen in der Weblayoutansicht ausgeblendet werden sollen. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | Ruft ab oder legt fest, ob die Inhaltsverzeichniseinträge als Hyperlinks dargestellt werden sollen. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | Ruft einen Ebenenbereich der Inhaltsverzeichniseinträge ab oder legt diesen fest, ab dem Seitenzahlen weggelassen werden sollen. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | Ruft die Kennung einer Sequenz ab oder legt sie fest, bei der der Seitenzahl des Eintrags ein Präfix hinzugefügt werden soll. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | Ruft ab oder legt fest, ob Zeilenumbruchzeichen innerhalb von Tabelleneinträgen beibehalten werden sollen. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | Ruft ab oder legt fest, ob Tabulatoreinträge innerhalb von Tabelleneinträgen beibehalten werden sollen. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die zum Trennen von Sequenznummern und Seitenzahlen verwendet wird. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | Ruft den Namen der Sequenzkennung ab, die beim Erstellen eines Abbildungsverzeichnisses verwendet wird, oder legt diesen fest. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | Ruft ab oder legt fest, ob die angewendete Absatzgliederungsebene verwendet werden soll. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | Aktualisiert die Seitenzahlen für Elemente in diesem Inhaltsverzeichnis. |

## Bemerkungen

Erstellt ein Inhaltsverzeichnis (das auch ein Abbildungsverzeichnis sein kann) unter Verwendung der durch TC-Felder angegebenen Einträge, ihrer Überschriftenebenen und angegebenen Stile und fügt diese Tabelle an dieser Stelle im Dokument ein.

## Beispiele

Zeigt, wie Sie ein Inhaltsverzeichnis einfügen und es mit Einträgen basierend auf Überschriftenstilen füllen.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Fügen Sie ein TOC-Feld ein, das alle Überschriften in einem Inhaltsverzeichnis zusammenfasst.
    // Für jede Überschrift erstellt dieses Feld eine Zeile mit dem Text in diesem Überschriftenstil auf der linken Seite.
    // und rechts die Seite, auf der die Überschrift erscheint.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Verwenden Sie die Eigenschaft BookmarkName, um nur Überschriften aufzulisten
    // die innerhalb der Grenzen eines Lesezeichens mit dem Namen „MyBookmark“ erscheinen.
    field.BookmarkName = "MyBookmark";

    // Text mit einem integrierten Überschriftenstil, z. B. „Überschrift 1“, wird als Überschrift gezählt.
    // In dieser Eigenschaft und den Inhaltsverzeichnisebenen können wir weitere Stile benennen, die als Überschriften vom Inhaltsverzeichnis übernommen werden sollen.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Standardmäßig werden Stile/Inhaltsverzeichnisebenen in der Eigenschaft „CustomStyles“ durch ein Komma getrennt.
    // aber wir können in dieser Eigenschaft ein benutzerdefiniertes Trennzeichen festlegen.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Konfigurieren Sie das Feld so, dass alle Überschriften ausgeschlossen werden, deren Inhaltsverzeichnisebenen außerhalb dieses Bereichs liegen.
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

    // Bei diesen beiden Überschriften werden die Seitenzahlen weggelassen, da sie im Bereich „2-5“ liegen.
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Dieser Eintrag wird nicht angezeigt, da „Überschrift 4“ außerhalb des zuvor festgelegten Bereichs „1–3“ liegt.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Dieser Eintrag wird nicht angezeigt, da er außerhalb des im Inhaltsverzeichnis angegebenen Lesezeichens liegt.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Beginnen Sie eine neue Seite und fügen Sie einen Absatz im angegebenen Stil ein.
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

Zeigt, wie ein Inhaltsverzeichnisfeld mithilfe von SEQ-Feldern mit Einträgen gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält, und die Seitennummer, auf der das Feld erscheint.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählungen für jede eindeutige benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Verwenden Sie die Eigenschaft „TableOfFiguresLabel“, um eine Hauptsequenz für das Inhaltsverzeichnis zu benennen.
// Jetzt erstellt dieses Inhaltsverzeichnis nur Einträge aus SEQ-Feldern, deren „SequenceIdentifier“ auf „MySequence“ gesetzt ist.
fieldToc.TableOfFiguresLabel = "MySequence";

// Wir können in der Eigenschaft „PrefixedSequenceIdentifier“ eine andere SEQ-Feldsequenz benennen.
    // SEQ-Felder aus dieser Präfixsequenz erstellen keine TOC-Einträge.
// Jeder TOC-Eintrag, der aus einem SEQ-Feld der Hauptsequenz erstellt wird, zeigt jetzt auch die Anzahl an,
// Die Präfixsequenz befindet sich derzeit im SEQ-Feld der Primärsequenz, das den Eintrag vorgenommen hat.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Jeder Inhaltsverzeichniseintrag zeigt die Anzahl der Präfixsequenzen unmittelbar links an
// der Seitenzahl, auf der das SEQ-Feld der Hauptsequenz erscheint.
// Wir können ein benutzerdefiniertes Trennzeichen angeben, das zwischen diesen beiden Zahlen angezeigt wird.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Es gibt zwei Möglichkeiten, SEQ-Felder zum Füllen dieses Inhaltsverzeichnisses zu verwenden.
// 1 - Einfügen eines SEQ-Feldes, das zur Präfixsequenz des Inhaltsverzeichnisses gehört:
// Dieses Feld erhöht die SEQ-Sequenzanzahl für „PrefixSequence“ um 1.
// Da dieses Feld nicht zur Hauptsequenz gehört, identifiziert
// durch die Eigenschaft „TableOfFiguresLabel“ des Inhaltsverzeichnisses wird es nicht als Eintrag angezeigt.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Einfügen eines SEQ-Feldes, das zur Hauptsequenz des Inhaltsverzeichnisses gehört:
// Dieses SEQ-Feld erstellt einen Eintrag im Inhaltsverzeichnis.
// Der Inhaltsverzeichniseintrag enthält den Absatz, in dem sich das SEQ-Feld befindet, und die Nummer der Seite, auf der es erscheint.
// Dieser Eintrag zeigt auch die aktuelle Anzahl der Präfixsequenzen an.
// durch den Wert in der SeqenceSeparator-Eigenschaft des Inhaltsverzeichnisses von der Seitenzahl getrennt.
// Der Zähler "PrefixSequence" steht bei 1, dieses Hauptsequenz-SEQ-Feld befindet sich auf Seite 2,
// und das Trennzeichen ist „>“, daher wird der Eintrag „1>2“ anzeigen.
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Seite einfügen, Präfixsequenz um 2 erhöhen und anschließend ein SEQ-Feld einfügen, um einen TOC-Eintrag zu erstellen.
// Die Präfixsequenz steht jetzt bei 2 und das SEQ-Feld der Hauptsequenz befindet sich auf Seite 3.
// daher wird im Inhaltsverzeichniseintrag als Seitenanzahl „2>3“ angezeigt.
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

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
