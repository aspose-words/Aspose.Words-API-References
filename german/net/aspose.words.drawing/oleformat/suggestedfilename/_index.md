---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: Aspose.Words für .NET
description: OleFormat SuggestedFileName eigendom. Ruft den für das aktuell eingebettete Objekt vorgeschlagenen Dateinamen ab wenn Sie es in einer Datei speichern möchten in C#.
type: docs
weight: 130
url: /de/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Ruft den für das aktuell eingebettete Objekt vorgeschlagenen Dateinamen ab, wenn Sie es in einer Datei speichern möchten.

```csharp
public string SuggestedFileName { get; }
```

## Beispiele

Zeigt, wie der vorgeschlagene Dateiname eines OLE-Objekts abgerufen wird.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape) doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// OLE-Objekte können einen vorgeschlagenen Dateinamen und eine Dateierweiterung bereitstellen,
// was wir verwenden können, wenn wir den Inhalt des Objekts in einer Datei im lokalen Dateisystem speichern.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### Siehe auch

* class [OleFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
