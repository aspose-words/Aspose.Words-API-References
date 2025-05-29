---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Border DistanceFromText“, um den Rahmenabstand von Text- oder Seitenrändern einfach in Punkten anzupassen und so die Layoutkontrolle zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Ruft den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten ab oder legt ihn fest.

```csharp
public double DistanceFromText { get; set; }
```

## Bemerkungen

Hat keine Auswirkung und wird für die Ränder von Tabellenzellen automatisch auf Null zurückgesetzt.

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

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
