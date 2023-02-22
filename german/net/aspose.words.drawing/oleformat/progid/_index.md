---
title: OleFormat.ProgId
second_title: Aspose.Words für .NET-API-Referenz
description: OleFormat eigendom. Ruft die ProgID des OLEObjekts ab oder legt sie fest.
type: docs
weight: 90
url: /de/net/aspose.words.drawing/oleformat/progid/
---
## OleFormat.ProgId property

Ruft die ProgID des OLE-Objekts ab oder legt sie fest.

```csharp
public string ProgId { get; set; }
```

### Bemerkungen

Die ProgID-Eigenschaft ist in Microsoft Word-Dokumenten nicht immer vorhanden und kann nicht zuverlässig verwendet werden.

Kann nicht Null sein.

Der Standardwert ist eine leere Zeichenfolge.

### Beispiele

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// Das OLE-Objekt in der ersten Form ist eine Microsoft Excel-Tabelle.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Unser Objekt wird weder automatisch aktualisiert noch vor Updates gesperrt.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Wenn wir das OLE-Objekt in einer Datei im lokalen Dateisystem speichern möchten,
// Wir können die Eigenschaft "SuggestedExtension" verwenden, um zu bestimmen, welche Dateierweiterung auf die Datei angewendet werden soll.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Im Folgenden finden Sie zwei Möglichkeiten, ein OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern.
// 1 - Über einen Stream speichern:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Speichern Sie es direkt unter einem Dateinamen:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Siehe auch

* class [OleFormat](../)
* namensraum [Aspose.Words.Drawing](../../oleformat/)
* Montage [Aspose.Words](../../../)


