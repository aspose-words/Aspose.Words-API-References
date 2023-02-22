---
title: FieldRef.IncludeNoteOrComment
second_title: Aspose.Words für .NET-API-Referenz
description: FieldRef eigendom. Ruft ab oder legt fest ob Fußnoten Endnoten und Anmerkungsnummern erhöht werden sollen die durch das Lesezeichen markiert sind und die entsprechenden Fußnoten Endnoten und Kommentartexte eingefügt werden.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldref/includenoteorcomment/
---
## FieldRef.IncludeNoteOrComment property

Ruft ab oder legt fest, ob Fußnoten-, Endnoten- und Anmerkungsnummern erhöht werden sollen, die durch das Lesezeichen markiert sind, und die entsprechenden Fußnoten-, Endnoten- und Kommentartexte eingefügt werden.

```csharp
public bool IncludeNoteOrComment { get; set; }
```

### Beispiele

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

* class [FieldRef](../)
* namensraum [Aspose.Words.Fields](../../fieldref/)
* Montage [Aspose.Words](../../../)


