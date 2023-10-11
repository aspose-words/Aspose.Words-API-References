---
title: Border.DistanceFromText
second_title: Aspose.Words für .NET-API-Referenz
description: Border eigendom. Ermittelt oder legt den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten fest.
type: docs
weight: 20
url: /de/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Ermittelt oder legt den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten fest.

```csharp
public double DistanceFromText { get; set; }
```

### Bemerkungen

Hat keine Auswirkung und wird für Ränder von Tabellenzellen automatisch auf Null zurückgesetzt.

### Beispiele

Zeigt, wie man oben auf der ersten Seite einen breiten blauen Bandrand erstellt.

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
* namensraum [Aspose.Words](../../border/)
* Montage [Aspose.Words](../../../)


