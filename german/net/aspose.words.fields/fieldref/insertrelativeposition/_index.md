---
title: FieldRef.InsertRelativePosition
linktitle: InsertRelativePosition
articleTitle: InsertRelativePosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldRef-Eigenschaft „InsertRelativePosition“ und verwalten Sie ganz einfach die Absatzpositionierung für eine verbesserte Dokumentformatierung und Lesbarkeit.
type: docs
weight: 80
url: /de/net/aspose.words.fields/fieldref/insertrelativeposition/
---
## FieldRef.InsertRelativePosition property

Ruft ab oder legt fest, ob die relative Position des referenzierten Absatzes eingefügt werden soll.

```csharp
public bool InsertRelativePosition { get; set; }
```

## Beispiele

Zeigt, wie REF-Felder zum Verweisen auf Lesezeichen eingefügt werden.

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

    // Zeigt die Listennummer des Lesezeichens an, wobei jedoch Nicht-Trennzeichen wie etwa spitze Klammern weggelassen werden.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Eine Listenebene nach unten gehen.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Zeigt die Listennummer des Lesezeichens und die Nummern aller darüber liegenden Listenebenen an.
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
/// Lassen Sie den Dokumentgenerator ein REF-Feld einfügen, damit auf ein Lesezeichen verweisen und davor und danach Text hinzufügen.
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
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
