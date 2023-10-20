---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words für .NET
description: Paragraph GetEffectiveTabStops methode. Gibt ein Array aller Tabstopps zurück die auf diesen Absatz angewendet werden einschließlich indirekter Tabstopps durch Stile oder Listen in C#.
type: docs
weight: 250
url: /de/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet werden, einschließlich indirekter Tabstopps durch Stile oder Listen.

```csharp
public TabStop[] GetEffectiveTabStops()
```

## Beispiele

Zeigt, wie Sie benutzerdefinierte Tabstopps für einen Absatz festlegen.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Wenn wir uns in einem Absatz ohne Tabstopps in dieser Sammlung befinden,
// Der Cursor springt jedes Mal um 36 Punkte, wenn wir in Microsoft Word die Tab-Taste drücken.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Wir können benutzerdefinierte Tabstopps in Microsoft Word hinzufügen, wenn wir das Lineal über die Registerkarte „Ansicht“ aktivieren.
// Jede Einheit auf diesem Lineal besteht aus zwei Standard-Tabstopps, also 72 Punkten.
// Wir können so programmgesteuert benutzerdefinierte Tabstopps hinzufügen.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Wir können diese Tabstopps in Microsoft Word sehen, indem wir das Lineal über „Ansicht“ -> aktivieren. „Anzeigen“ -> "Herrscher".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Alle von uns hinzugefügten Tabulatorzeichen nutzen die Tabstopps auf dem Lineal und können,
// Lassen Sie abhängig vom Wert des Tab-Vorspanns eine Zeile zwischen den Tab-Abfahrts- und Ankunftszielen.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Siehe auch

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
