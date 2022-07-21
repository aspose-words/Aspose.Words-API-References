---
title: FieldRef
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das REF-Feld.
type: docs
weight: 2180
url: /de/net/aspose.words.fields/fieldref/
---
## FieldRef class

Implementiert das REF-Feld.

```csharp
public class FieldRef : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldRef](fieldref)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldref/bookmarkname) { get; set; } | Ruft den Namen des referenzierten Lesezeichens ab oder legt ihn fest. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format) { get; } | erhält a[`FieldFormat`](../fieldformat) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IncludeNoteOrComment](../../aspose.words.fields/fieldref/includenoteorcomment) { get; set; } | Ruft ab oder legt fest, ob Fußnoten-, Endnoten- und Anmerkungsnummern erhöht werden sollen, die durch das Lesezeichen markiert sind, und die entsprechenden Fußnoten-, Endnoten- und Kommentartexte eingefügt werden. |
| [InsertHyperlink](../../aspose.words.fields/fieldref/inserthyperlink) { get; set; } | Ruft ab oder legt fest, ob ein Hyperlink zum mit Lesezeichen versehenen Absatz erstellt werden soll. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldref/insertparagraphnumber) { get; set; } | Ermittelt oder legt fest, ob die Absatznummer des referenzierten Absatzes genau so eingefügt werden soll, wie sie im Dokument erscheint. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldref/insertparagraphnumberinfullcontext) { get; set; } | Ruft ab oder legt fest, ob die Absatznummer des referenzierten Absatzes im vollständigen Kontext eingefügt werden soll. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldref/insertparagraphnumberinrelativecontext) { get; set; } | Ruft ab oder legt fest, ob die Absatznummer des referenzierten Absatzes in relativen Kontext eingefügt werden soll. |
| [InsertRelativePosition](../../aspose.words.fields/fieldref/insertrelativeposition) { get; set; } | Ruft ab oder legt fest, ob die relative Position des referenzierten Absatzes eingefügt werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [NumberSeparator](../../aspose.words.fields/fieldref/numberseparator) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldref/suppressnondelimiters) { get; set; } | Ruft ab oder legt fest, ob Nicht-Trennzeichen unterdrückt werden sollen. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Fügt den Text oder die Grafiken ein, die durch das angegebene Lesezeichen dargestellt werden.

### Beispiele

Zeigt, wie Text mit Lesezeichen mit einem SET-Feld erstellt und dann mit einem REF-Feld im Dokument angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Markierten Text mit einem SET-Feld benennen.
// Dieses Feld bezieht sich auf das "Lesezeichen", nicht auf eine Lesezeichenstruktur, die im Text erscheint, sondern auf eine benannte Variable.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Auf das Lesezeichen nach Namen in einem REF-Feld verweisen und seinen Inhalt anzeigen.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

Zeigt, wie REF-Felder eingefügt werden, um auf Lesezeichen zu verweisen.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // Wir wenden ein benutzerdefiniertes Listenformat an, bei dem die Anzahl der spitzen Klammern die Listenebene angibt, auf der wir uns gerade befinden.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Ein REF-Feld einfügen, das den Text in unserem Lesezeichen enthält, als Hyperlink fungiert und die Fußnoten des Lesezeichens klont.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Ein REF-Feld einfügen und anzeigen, ob sich das referenzierte Lesezeichen darüber oder darunter befindet.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Die Listennummer des Lesezeichens anzeigen, wie sie im Dokument erscheint.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Zeigt die Listennummer des Lesezeichens an, aber ohne Trennzeichen, wie z. B. die spitzen Klammern.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Eine Listenebene nach unten verschieben.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Anzeige der Listennummer des Lesezeichens und der Nummern aller darüber liegenden Listenebenen.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Zeigt die Nummern der Listenebene zwischen diesem REF-Feld und dem Lesezeichen an, auf das es verweist.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // Am Ende des Dokuments wird das Lesezeichen hier als Listenelement angezeigt.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");

/// <summary>
/// Lassen Sie den Document Builder ein REF-Feld einfügen, verweisen Sie damit auf ein Lesezeichen und fügen Sie davor und danach Text hinzu.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### Siehe auch

* class [Field](../field)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
