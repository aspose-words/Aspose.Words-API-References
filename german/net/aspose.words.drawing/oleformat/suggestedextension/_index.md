---
title: OleFormat.SuggestedExtension
linktitle: SuggestedExtension
articleTitle: SuggestedExtension
second_title: Aspose.Words für .NET
description: OleFormat SuggestedExtension eigendom. Ruft die für das aktuell eingebettete Objekt vorgeschlagene Dateierweiterung ab wenn Sie es in einer Datei speichern möchten in C#.
type: docs
weight: 120
url: /de/net/aspose.words.drawing/oleformat/suggestedextension/
---
## OleFormat.SuggestedExtension property

Ruft die für das aktuell eingebettete Objekt vorgeschlagene Dateierweiterung ab, wenn Sie es in einer Datei speichern möchten.

```csharp
public string SuggestedExtension { get; }
```

## Beispiele

Zeigt, wie eingebettete OLE-Objekte in Dateien extrahiert werden.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// Das OLE-Objekt in der ersten Form ist eine Microsoft Excel-Tabelle.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Unser Objekt wird weder automatisch aktualisiert noch für Aktualisierungen gesperrt.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Wenn wir planen, das OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern,
// Wir können die Eigenschaft „SuggestedExtension“ verwenden, um zu bestimmen, welche Dateierweiterung auf die Datei angewendet werden soll.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Nachfolgend finden Sie zwei Möglichkeiten, ein OLE-Objekt in einer Datei im lokalen Dateisystem zu speichern.
// 1 - Über einen Stream speichern:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 – Direkt unter einem Dateinamen speichern:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Siehe auch

* class [OleFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
