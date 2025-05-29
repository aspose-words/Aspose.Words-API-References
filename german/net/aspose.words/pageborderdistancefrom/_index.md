---
title: PageBorderDistanceFrom Enum
linktitle: PageBorderDistanceFrom
articleTitle: PageBorderDistanceFrom
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.PageBorderDistanceFrom für eine präzise Platzierung der Seitenränder. Verbessern Sie die Dokumentformatierung durch optimale Randpositionierung.
type: docs
weight: 5080
url: /de/net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

Gibt die Positionierung des Seitenrahmens relativ zum Seitenrand an.

```csharp
public enum PageBorderDistanceFrom
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | `0` | Die Rahmenposition wird vom Seitenrand aus gemessen. |
| PageEdge | `1` | Die Randposition wird vom Seitenrand aus gemessen. |

## Beispiele

Zeigt, wie oben auf der ersten Seite ein breiter blauer Bandrand erstellt wird.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Siehe auch

* class [PageSetup](../pagesetup/)
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
