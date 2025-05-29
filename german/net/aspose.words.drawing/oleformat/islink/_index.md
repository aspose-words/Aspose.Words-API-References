---
title: OleFormat.IsLink
linktitle: IsLink
articleTitle: IsLink
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsLink-Eigenschaft von OleFormat. Überprüfen Sie einfach, ob Ihr OLE-Objekt mit SourceFullName verknüpft ist, um eine nahtlose Datenintegration und -verwaltung zu gewährleisten.
type: docs
weight: 40
url: /de/net/aspose.words.drawing/oleformat/islink/
---
## OleFormat.IsLink property

Rückgaben`WAHR` wenn das OLE-Objekt verknüpft ist (wenn[`SourceFullName`](../sourcefullname/) angegeben ist).

```csharp
public bool IsLink { get; }
```

## Beispiele

Zeigt, wie verknüpfte und nicht verknüpfte OLE-Objekte eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Betten Sie eine Microsoft Visio-Zeichnung als OLE-Objekt in das Dokument ein.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Fügen Sie einen Link zur Datei im lokalen Dateisystem ein und zeigen Sie ihn als Symbol an.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// Durch das Einfügen von OLE-Objekten werden Formen erstellt, die diese Objekte speichern.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Wenn eine Form ein OLE-Objekt enthält, verfügt sie über eine gültige "OleFormat"-Eigenschaft,
// die wir verwenden können, um einige Aspekte der Form zu überprüfen.
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
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
