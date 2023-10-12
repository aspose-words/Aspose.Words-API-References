---
title: OleFormat.IsLink
second_title: Aspose.Words für .NET-API-Referenz
description: OleFormat eigendom. Gibt zurückWAHR ob das OLEObjekt verknüpft ist wannSourceFullName angegeben ist.
type: docs
weight: 40
url: /de/net/aspose.words.drawing/oleformat/islink/
---
## OleFormat.IsLink property

Gibt zurück`WAHR` ob das OLE-Objekt verknüpft ist (wann[`SourceFullName`](../sourcefullname/) angegeben ist).

```csharp
public bool IsLink { get; }
```

### Beispiele

Zeigt, wie verknüpfte und nicht verknüpfte OLE-Objekte eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Microsoft Visio-Zeichnung als OLE-Objekt in das Dokument einbetten.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Einen Link zur Datei im lokalen Dateisystem einfügen und als Symbol anzeigen.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// Durch das Einfügen von OLE-Objekten werden Formen erstellt, die diese Objekte speichern.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Wenn eine Form ein OLE-Objekt enthält, verfügt sie über eine gültige „OleFormat“-Eigenschaft.
// mit dem wir einige Aspekte der Form überprüfen können.
OleFormat oleFormat = shapes[0].OleFormat;

Assert.AreEqual(false, oleFormat.IsLink);
Assert.AreEqual(false, oleFormat.OleIcon);

oleFormat = shapes[1].OleFormat;

Assert.AreEqual(true, oleFormat.IsLink);
Assert.AreEqual(true, oleFormat.OleIcon);

Assert.True(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"));
Assert.AreEqual("", oleFormat.SourceItem);

Assert.AreEqual("Microsoft Visio drawing.vsd", oleFormat.IconCaption);

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// Wenn das Objekt OLE-Daten enthält, können wir über einen Stream darauf zugreifen.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### Siehe auch

* class [OleFormat](../)
* namensraum [Aspose.Words.Drawing](../../oleformat/)
* Montage [Aspose.Words](../../../)


