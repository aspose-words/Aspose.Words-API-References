---
title: FieldSeq.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words für .NET
description: FieldSeq BookmarkName eigendom. Ruft einen Lesezeichennamen ab oder legt diesen fest der auf ein Element an einer anderen Stelle im Dokument und nicht an der aktuellen Position verweist in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Ruft einen Lesezeichennamen ab oder legt diesen fest, der auf ein Element an einer anderen Stelle im Dokument und nicht an der aktuellen Position verweist.

```csharp
public string BookmarkName { get; set; }
```

## Beispiele

Zeigt, wie Inhaltsverzeichnis- und Sequenzfelder kombiniert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält,
// und die Nummer der Seite, auf der das Feld erscheint.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Konfigurieren Sie dieses TOC-Feld so, dass es eine SequenceIdentifier-Eigenschaft mit dem Wert „MySequence“ hat.
fieldToc.TableOfFiguresLabel = "MySequence";

// Dieses TOC-Feld so konfigurieren, dass es nur SEQ-Felder aufnimmt, die innerhalb der Grenzen eines Lesezeichens liegen
// mit dem Namen „TOCBookmark“.
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählwerte für jede eindeutig benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Fügen Sie ein SEQ-Feld ein, das einen Sequenzbezeichner hat, der mit den Inhaltsverzeichnissen übereinstimmt
// TableOfFiguresLabel-Eigenschaft. Dieses Feld erstellt keinen Eintrag im Inhaltsverzeichnis, da es außerhalb liegt
// die durch „BookmarkName“ bezeichneten Grenzen des Lesezeichens.
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Die Sequenz dieses SEQ-Felds entspricht der „TableOfFiguresLabel“-Eigenschaft des Inhaltsverzeichnisses und liegt innerhalb der Lesezeichengrenzen.
// Der Absatz, der dieses Feld enthält, wird im Inhaltsverzeichnis als Eintrag angezeigt.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Die Sequenz dieses SEQ-Felds stimmt nicht mit der „TableOfFiguresLabel“-Eigenschaft des Inhaltsverzeichnisses überein.
// und liegt innerhalb der Grenzen des Lesezeichens. Der zugehörige Absatz wird im Inhaltsverzeichnis nicht als Eintrag angezeigt.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Die Sequenz dieses SEQ-Felds entspricht der „TableOfFiguresLabel“-Eigenschaft des Inhaltsverzeichnisses und liegt innerhalb der Grenzen des Lesezeichens.
// Dieses Feld verweist auch auf ein anderes Lesezeichen. Der Inhalt dieses Lesezeichens wird im TOC-Eintrag für dieses SEQ-Feld angezeigt.
// Das SEQ-Feld selbst zeigt den Inhalt dieses Lesezeichens nicht an.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Erstellen Sie ein Lesezeichen mit Inhalten, die im TOC-Eintrag angezeigt werden, da das obige SEQ-Feld darauf verweist.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

### Siehe auch

* class [FieldSeq](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
