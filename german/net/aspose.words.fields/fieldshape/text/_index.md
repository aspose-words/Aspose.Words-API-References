---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Verwalten Sie FieldShape-Text ganz einfach – rufen Sie Werte mühelos ab oder legen Sie sie fest, um einen nahtlosen Datenabruf und eine verbesserte Funktionalität in Ihren Anwendungen zu ermöglichen.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

Ruft den abzurufenden Text ab oder legt ihn fest.

```csharp
public string Text { get; set; }
```

## Beispiele

Zeigt, wie man mit BIDIOUTLINE-Feldern sprachkompatible Listen von rechts nach links erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das Feld BIDIOUTLINE nummeriert Absätze wie die Felder AUTONUM/LISTNUM,
// ist aber nur sichtbar, wenn eine von rechts nach links geschriebene Bearbeitungssprache aktiviert ist, beispielsweise Hebräisch oder Arabisch.
// Das folgende Feld zeigt „.1“ an, das RTL-Äquivalent der Listennummer „1.“.
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Fügen Sie zwei weitere BIDIOUTLINE-Felder hinzu, die „.2“ und „.3“ anzeigen.
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Stellen Sie die horizontale Textausrichtung für jeden Absatz im Dokument auf RTL ein.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Wenn wir in Microsoft Word eine Bearbeitungssprache mit Schreibrichtung von rechts nach links aktivieren, werden in unseren Feldern Zahlen angezeigt.
// Andernfalls wird „###“ angezeigt.
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Zeigt, wie einige ältere Microsoft Word-Felder wie SHAPE und EMBED beim Laden behandelt werden.

```csharp
// Öffnen Sie ein Dokument, das in Microsoft Word 2003 erstellt wurde.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Wenn wir das Word-Dokument öffnen und Alt+F9 drücken, sehen wir ein SHAPE- und ein EMBED-Feld.
// Ein SHAPE-Feld ist der Anker/die Leinwand für ein AutoShape-Objekt mit aktiviertem Umbruchstil „In Zeile mit Text“.
// Ein EMBED-Feld hat die gleiche Funktion, aber für ein eingebettetes Objekt,
// wie beispielsweise eine Tabelle aus einem externen Excel-Dokument.
// Diese Felder werden jedoch nicht in der Feldersammlung des Dokuments angezeigt.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Diese Felder werden nur von alten Versionen von Microsoft Word unterstützt.
// Der Dokumentladevorgang konvertiert diese Felder in Shape-Objekte.
// auf die wir in der Knotensammlung des Dokuments zugreifen können.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Der erste Shape-Knoten entspricht dem SHAPE-Feld im Eingabedokument.
// Dies ist die Inline-Leinwand für die AutoForm.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Der zweite Shape-Knoten ist die AutoShape selbst.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Die dritte Form ist das EMBED-Feld, das die externe Tabelle enthielt.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Siehe auch

* class [FieldShape](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
