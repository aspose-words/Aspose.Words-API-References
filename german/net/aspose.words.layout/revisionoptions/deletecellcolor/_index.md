---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: Aspose.Words für .NET
description: Passen Sie Ihre Tabelle mit der DeleteCellColor-Eigenschaft von RevisionOptions an. Legen Sie für gelöschte Zellen ganz einfach eine eindeutige Farbe fest und verbessern Sie so die Übersichtlichkeit und Organisation.
type: docs
weight: 20
url: /de/net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

Ermöglicht die Angabe der Farbe, die für gelöschte Zellen verwendet werden sollDeletion . Der Standardwert istPink .

```csharp
public RevisionColor DeleteCellColor { get; set; }
```

## Beispiele

Zeigt, wie mit der Revisionsfarbe für das Einfügen/Löschen von Zellen gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### Siehe auch

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
