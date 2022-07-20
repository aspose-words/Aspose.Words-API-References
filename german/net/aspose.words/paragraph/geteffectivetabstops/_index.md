---
title: GetEffectiveTabStops
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt ein Array aller Tabstopps zurück die auf diesen Absatz angewendet wurden einschließlich der indirekten Anwendung durch Stile oder Listen.
type: docs
weight: 250
url: /de/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet wurden, einschließlich der indirekten Anwendung durch Stile oder Listen.

```csharp
public TabStop[] GetEffectiveTabStops()
```

### Beispiele

Zeigt, wie benutzerdefinierte Tabstopps für einen Absatz festgelegt werden.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Wenn wir uns in einem Absatz ohne Tabstopps in dieser Sammlung befinden,
// Der Cursor springt jedes Mal um 36 Punkte, wenn wir die Tabulatortaste in Microsoft Word drücken.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Wir können benutzerdefinierte Tabstopps in Microsoft Word hinzufügen, wenn wir das Lineal über die Registerkarte "Ansicht" aktivieren.
// Jede Einheit auf diesem Lineal besteht aus zwei Standard-Tabstopps, was 72 Punkten entspricht.
// Wir können benutzerdefinierte Tabstopps programmgesteuert wie folgt hinzufügen.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Wir können diese Tabstopps in Microsoft Word sehen, indem wir das Lineal über "Ansicht" -> "Anzeigen" -> "Lineal".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Alle Tabulatorzeichen, die wir hinzufügen, verwenden die Tabstopps auf dem Lineal und können,
// Lassen Sie je nach Wert des Tab-Leaders eine Linie zwischen den Tab-Abfahrts- und -Ankunftszielen.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Siehe auch

* class [TabStop](../../tabstop)
* class [Paragraph](../../paragraph)
* namensraum [Aspose.Words](../../paragraph)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->