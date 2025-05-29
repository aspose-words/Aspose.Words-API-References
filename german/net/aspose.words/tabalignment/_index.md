---
title: TabAlignment Enum
linktitle: TabAlignment
articleTitle: TabAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.TabAlignment-Aufzählung für anpassbare Tabstopp-Ausrichtung. Verbessern Sie noch heute die Dokumentformatierung mit Präzision und Flexibilität!
type: docs
weight: 7030
url: /de/net/aspose.words/tabalignment/
---
## TabAlignment enumeration

Gibt die Ausrichtung/den Typ eines Tabulators an.

```csharp
public enum TabAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Left | `0` | Richtet den Text nach dem Tabulator linksbündig aus. |
| Center | `1` | Zentriert den Text um den Tabulator. |
| Right | `2` | Richtet den Text am Tabulator rechtsbündig aus. |
| Decimal | `3` | Richtet den Text am Dezimalpunkt aus. |
| Bar | `4` | Zeichnet einen vertikalen Strich an der Tabstoppposition. |
| List | `6` | Der Tabulator ist ein Trennzeichen zwischen der Zahl/dem Aufzählungszeichen und dem Text in einem Listenelement. |
| Clear | `7` | Löscht alle Tabulatoren an dieser Position. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
