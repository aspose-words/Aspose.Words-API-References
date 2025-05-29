---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: Aspose.Words für .NET
description: Entdecken Sie die OleFormat SuggestedFileName-Eigenschaft, um einfach den empfohlenen Dateinamen zum nahtlosen Speichern Ihrer eingebetteten Objekte abzurufen.
type: docs
weight: 130
url: /de/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Ruft den für das aktuelle eingebettete Objekt vorgeschlagenen Dateinamen ab, wenn Sie es in einer Datei speichern möchten.

```csharp
public string SuggestedFileName { get; }
```

## Beispiele

Zeigt, wie man den vorgeschlagenen Dateinamen eines OLE-Objekts erhält.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape)doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// OLE-Objekte können einen vorgeschlagenen Dateinamen und eine Erweiterung bereitstellen,
// die wir verwenden können, wenn wir den Inhalt des Objekts in einer Datei im lokalen Dateisystem speichern.
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
