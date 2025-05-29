---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode GetEffectiveTabStops, um alle Tabstopps in einem Absatz abzurufen, einschließlich derer aus Stilen und Listen für eine verbesserte Formatierung.
type: docs
weight: 270
url: /de/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet wurden, einschließlich derer, die indirekt durch Stile oder Listen angewendet wurden.

```csharp
public TabStop[] GetEffectiveTabStops()
```

## Beispiele

Zeigt, wie benutzerdefinierte Tabstopps für einen Absatz festgelegt werden.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Wenn wir uns in einem Absatz ohne Tabstopps in dieser Sammlung befinden,
// Der Cursor springt jedes Mal 36 Punkte, wenn wir in Microsoft Word die Tabulatortaste drücken.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Wir können in Microsoft Word benutzerdefinierte Tabstopps hinzufügen, wenn wir das Lineal über die Registerkarte „Ansicht“ aktivieren.
// Jede Einheit auf diesem Lineal besteht aus zwei Standardtabulatoren, also 72 Punkten.
// Wir können benutzerdefinierte Tabstopps programmgesteuert wie folgt hinzufügen.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Wir können diese Tabstopps in Microsoft Word sehen, indem wir das Lineal über „Ansicht“ -> „Anzeigen“ -> „Lineal“ aktivieren.
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Alle Tabulatorzeichen, die wir hinzufügen, nutzen die Tabulatoren auf dem Lineal und können
// Lassen Sie je nach Wert des Tabulatorführers eine Linie zwischen den Tabulator-Abfahrts- und Ankunftszielen.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Siehe auch

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
