---
title: Class FieldRef
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldRef klas. Implementiert das REFFeld.
type: docs
weight: 2330
url: /de/net/aspose.words.fields/fieldref/
---
## FieldRef class

Implementiert das REF-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldRef : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldRef](fieldref/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldref/bookmarkname/) { get; set; } | Ruft den Namen des referenzierten Lesezeichens ab oder legt diesen fest. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ruft a ab[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IncludeNoteOrComment](../../aspose.words.fields/fieldref/includenoteorcomment/) { get; set; } | Ruft ab oder legt fest, ob Fußnoten-, Endnoten- und Anmerkungsnummern erhöht werden sollen, die durch das Lesezeichen markiert sind, und der entsprechende Fußnoten-, Endnoten- und Kommentartext eingefügt werden soll. |
| [InsertHyperlink](../../aspose.words.fields/fieldref/inserthyperlink/) { get; set; } | Ruft ab oder legt fest, ob ein Hyperlink zum mit einem Lesezeichen versehenen Absatz erstellt werden soll. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldref/insertparagraphnumber/) { get; set; } | Ruft ab oder legt fest, ob die Absatznummer des referenzierten Absatzes genau so eingefügt werden soll, wie sie im Dokument erscheint. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/) { get; set; } | Ruft ab oder legt fest, ob die Absatznummer des referenzierten Absatzes im vollständigen Kontext eingefügt werden soll. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldref/insertparagraphnumberinrelativecontext/) { get; set; } | Ruft ab oder legt fest, ob die Absatznummer des referenzierten Absatzes im relativen Kontext eingefügt werden soll. |
| [InsertRelativePosition](../../aspose.words.fields/fieldref/insertrelativeposition/) { get; set; } | Ruft ab oder legt fest, ob die relative Position des referenzierten Absatzes eingefügt werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [NumberSeparator](../../aspose.words.fields/fieldref/numberseparator/) { get; set; } | Ruft die Zeichenfolge ab, die zum Trennen von Sequenznummern und Seitenzahlen verwendet wird, oder legt diese fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`Null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldref/suppressnondelimiters/) { get; set; } | Ruft ab oder legt fest, ob Zeichen ohne Trennzeichen unterdrückt werden sollen. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl der Feldcode als auch das Feldergebnis der untergeordneten Felder sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte child seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`Null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Fügt den durch das angegebene Lesezeichen dargestellten Text oder die Grafik ein.

### Beispiele

Zeigt, wie Sie mit einem SET-Feld markierten Text erstellen und ihn dann mithilfe eines REF-Felds im Dokument anzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Mit einem Lesezeichen versehenen Text mit einem SET-Feld benennen.
// Dieses Feld bezieht sich auf das „Lesezeichen“, nicht auf eine Lesezeichenstruktur, die im Text erscheint, sondern auf eine benannte Variable.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// In einem REF-Feld namentlich auf das Lesezeichen verweisen und seinen Inhalt anzeigen.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

Zeigt, wie REF-Felder zum Referenzieren von Lesezeichen eingefügt werden.

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

    // Wir werden ein benutzerdefiniertes Listenformat anwenden, wobei die Anzahl der spitzen Klammern die Listenebene angibt, auf der wir uns gerade befinden.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Fügen Sie ein REF-Feld ein, das den Text in unserem Lesezeichen enthält, als Hyperlink fungiert und die Fußnoten des Lesezeichens klont.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Ein REF-Feld einfügen und anzeigen, ob sich das referenzierte Lesezeichen darüber oder darunter befindet.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Zeigt die Listennummer des Lesezeichens an, wie sie im Dokument erscheint.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Zeigt die Listennummer des Lesezeichens an, jedoch ohne Trennzeichen, wie z. B. spitze Klammern.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Eine Listenebene nach unten verschieben.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Listennummer des Lesezeichens und die Nummern aller darüber liegenden Listenebenen anzeigen.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Zeigt die Listenebenennummern zwischen diesem REF-Feld und dem Lesezeichen an, auf das es verweist.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // Am Ende des Dokuments wird das Lesezeichen hier als Listenelement angezeigt.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// Veranlassen Sie den Document Builder, ein REF-Feld einzufügen, damit auf ein Lesezeichen zu verweisen und Text davor und danach hinzuzufügen.
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

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


